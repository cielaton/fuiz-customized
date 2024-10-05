<script lang="ts">
</script>

<div style:height="100%" style:width="100%" style:display="flex">
    <div id="image_wrapper">
        <!-- List all of the logos -->
        <img id="BKLogo" src="$lib/assets/BKLogo.jpg"/>
        <img id="DoanLogo" src="$lib/assets/DoanLogo.png"/>
        <img id="FASTLogo" src="$lib/assets/FASTLogo.png"/>
        <img id="UniquifyLogo" src="$lib/assets/UniquifyLogo.png"/>
    </div>
</div>

<style>
    #image_wrapper {
        padding: 0 20px 0 20px;
        margin-right: auto;
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: space-between;
        align-items: center;
    }

    #BKLogo {
        width: 15%;
    }

    #DoanLogo {
        width: 15%;
    }

    #FASTLogo {
        width: 30%;
    }

    #UniquifyLogo {
        width: 30%;
    }

    @media only screen and (min-width: 525px) {
        #BKLogo {
            height: 60px;
            width: auto;
            padding-left: 20px;
        }

        #DoanLogo {
            height: 60px;
            width: auto;
            padding-left: 20px;
        }

        #FASTLogo {
            height: 100px;
            width: auto;
            padding-left: 20px;
        }

        #UniquifyLogo {
            height: 50px;
            width: auto;
            padding-left: 20px;
        }
    }
</style>
