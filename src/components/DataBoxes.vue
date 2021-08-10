<template>
    <div>
        <div class="grid md:grid-cols-2 gap-4">
            <!-- box 1 -->
            <div class="shadow-md bg-blue-100 p-10 text-center rounded">
                <h3 class="text-3xl text-blue-900 font-bold mb-4">Cases</h3>
                <div class="text-2xl mb-4">
                    <span class="font-bold">New:</span>
                    {{stats.NewConfirmed.toLocaleString()}} 
                    <span class="text-red-400">Cases</span>
                </div>
                <div class="text-2xl mb-4">
                    <span class="font-bold">Total:</span>
                    {{stats.TotalConfirmed.toLocaleString()}}
                    <span class="text-red-400">Cases</span>
                </div>
            </div>
            <!-- Box 2 -->
            <div class="shadow-md bg-blue-200 p-10 text-center rounded">
                <h3 class="text-3xl text-blue-900 font-bold mb-4">Deaths</h3>
                <div class="text-2xl mb-4">
                    <span class="font-bold">New:</span>
                    {{stats.NewDeaths.toLocaleString()}} 
                    <span class="text-red-700">Deaths</span>
                </div>
                <div class="text-2xl mb-4">
                    <span class="font-bold">Total:</span>
                    {{stats.TotalDeaths.toLocaleString()}}
                    <span class="text-red-700">Deaths</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DataBoxes',
    props: ['stats'],
}
</script>