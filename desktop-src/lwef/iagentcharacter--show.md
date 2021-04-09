---
title: IAgentCharacter mostrar
description: IAgentCharacter mostrar
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007551"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="eecfd-103">IAgentCharacter:: mostrar</span><span class="sxs-lookup"><span data-stu-id="eecfd-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="eecfd-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eecfd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="eecfd-105">Exibe um caractere.</span><span class="sxs-lookup"><span data-stu-id="eecfd-105">Displays a character.</span></span>

-   <span data-ttu-id="eecfd-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="eecfd-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="eecfd-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="eecfd-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="eecfd-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="eecfd-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="eecfd-109">Sinalizador de animação de estado de exibição.</span><span class="sxs-lookup"><span data-stu-id="eecfd-109">Showing state animation flag.</span></span> <span data-ttu-id="eecfd-110">Se esse parâmetro for **true**, a animação de estado de **exibição** será reproduzida depois de tornar o caractere visível; Se **for false**, a animação não será reproduzida.</span><span class="sxs-lookup"><span data-stu-id="eecfd-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="eecfd-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="eecfd-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="eecfd-112">Endereço de uma variável que recebe a ID da solicitação de [**exibição**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="eecfd-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="eecfd-113">Evite definir o parâmetro *bFast* como **true** sem reproduzir uma animação com antecedência. caso contrário, o quadro de caracteres poderá ser exibido, mas não terá nenhuma imagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="eecfd-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="eecfd-114">Em particular, observe que, se você chamar [**MoveTo**](iagentcharacter--moveto.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação.</span><span class="sxs-lookup"><span data-stu-id="eecfd-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="eecfd-115">Portanto, se você chamar o método **show** com *BFast* definido como **true**, nenhuma imagem será exibida.</span><span class="sxs-lookup"><span data-stu-id="eecfd-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="eecfd-116">Da mesma forma, se você chamar [**ocultar**](/windows/desktop/lwef/iagentcharacter--hide)e, em seguida, **Mostrar** com *bFast* definido como **true**, não haverá imagem visível.</span><span class="sxs-lookup"><span data-stu-id="eecfd-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="eecfd-117">Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade da animação de estado **mostrando** antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="eecfd-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="eecfd-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eecfd-118">See Also</span></span>

[<span data-ttu-id="eecfd-119">**IAgentCharacter:: Hide**</span><span class="sxs-lookup"><span data-stu-id="eecfd-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 