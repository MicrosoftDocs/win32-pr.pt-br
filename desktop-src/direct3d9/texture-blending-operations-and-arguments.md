---
description: Os aplicativos associam um estágio de mesclagem a cada textura no conjunto de texturas atuais. O Direct3D avalia cada estágio de mesclagem na ordem, começando pela primeira textura no conjunto e terminando com oitavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operações e argumentos de mesclagem de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791662"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="f1e5a-104">Operações e argumentos de mesclagem de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f1e5a-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="f1e5a-105">Os aplicativos associam um estágio de mesclagem a cada textura no conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="f1e5a-106">O Direct3D avalia cada estágio de mesclagem na ordem, começando pela primeira textura no conjunto e terminando com oitavo.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="f1e5a-107">O Direct3D aplica as informações de cada textura no conjunto de texturas atuais ao estágio de mesclagem associado a ela.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="f1e5a-108">Os aplicativos controlam quais informações de um estágio de textura são usadas chamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="f1e5a-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="f1e5a-109">Você pode definir operações separadas para os canais de cor e alfa, e cada operação usa dois argumentos.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="f1e5a-110">Especifique as operações de canal de cores usando o \_ estado de estágio D3DTSS COLOROP; especifique operações alfa usando D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="f1e5a-111">Ambos os Estados de estágio usam valores do tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="f1e5a-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="f1e5a-112">Os argumentos de mesclagem de textura usam os \_ Membros D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 e D3DTSS \_ ALPHARG2 do tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="f1e5a-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="f1e5a-113">Os valores de argumento correspondentes são identificados usando [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="f1e5a-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="f1e5a-114">Você pode desabilitar um estágio de textura e quaisquer estágios de mesclagem de textura subsequentes na cascata, definindo a operação de cor para esse estágio como D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="f1e5a-115">Desabilitar a operação de cor efetivamente desabilita a operação alfa também.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="f1e5a-116">As operações alfa não podem ser desabilitadas quando as operações de cores estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="f1e5a-117">Definir a operação Alpha como D3DTOP \_ Disable quando a mesclagem de cores está habilitada causa um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="f1e5a-118">Para determinar as operações de mesclagem de textura com suporte de um dispositivo, consulte o membro TextureCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="f1e5a-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1e5a-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1e5a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e5a-120">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="f1e5a-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
