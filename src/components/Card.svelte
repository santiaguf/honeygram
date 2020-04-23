<script>
    import Comments from './Comments.svelte';
</script>

<div class="Card">
    <div class="Card-container">
        <div class="Card-header">
            <div class="Card-user">
                <img src="../public/images/honey1.png" alt="">
                <h2>Honey.Michifu</h2>
                <span>Pereira, Colombia</span>
            </div>
            <div class="Card-settings">
                <i class="fas fa-ellipsis-h" />
            </div>
        </div>
        <div class="Card-photo">
            <figure>
                <img src="../public/images/honey1.png" alt="">    
            </figure>
        </div>
        <div class="Card-icons">
            <div class="Card-icons-first">
                <i class="fas fa-heart" />
                <i class="fas fa-paper-plane" />
            </div>
            <div class="Card-icons-second">
                <i class="fas fa-bookmark" />
            </div>
        </div>
        <div class="Card-description">
            <h3>Honey.Michifu</h3>
            <span>Hola!!</span>
        </div>
        <Comments />
    </div>
</div>