<template>
    <div class="p-2">
        <chat-message v-for="(message, index) in messages" :message="message" :key="index"></chat-message>
    </div>
</template>

<script lang="ts">
import ChatMessage from "~/components/atoms/ChatMessage.vue"
import Message from "~/models/message"

export default {
    data() {
        return {
            messages: [
                new Message(new Date(), "Joe", "Hey bob!"),
                new Message(new Date(), "Bob", "Hey Joe, what's up?"),
                new Message(new Date(), "Joe", "Not much bro!"),
            ],
        }
    },
    components: {
        ChatMessage
    }
}
</script>