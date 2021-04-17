---
title: Network. bufferingTime
description: A propriedade bufferingTime especifica ou recupera a quantidade de tempo em milissegundos alocada para armazenar em buffer os dados de entrada antes do início da execução.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network. bufferingTime Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761069"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="71e77-104">Network. bufferingTime</span><span class="sxs-lookup"><span data-stu-id="71e77-104">Network.bufferingTime</span></span>

<span data-ttu-id="71e77-105">A propriedade **bufferingTime** especifica ou recupera a quantidade de tempo em milissegundos alocada para armazenar em buffer os dados de entrada antes do início da execução.</span><span class="sxs-lookup"><span data-stu-id="71e77-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e77-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71e77-106">Syntax</span></span>

<span data-ttu-id="71e77-107">*Player*. *rede*. **bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="71e77-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="71e77-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="71e77-108">Possible Values</span></span>

<span data-ttu-id="71e77-109">Essa propriedade é um **número** de leitura/gravação (**longo**) que varia de zero a 60.000 com um valor padrão de 5.000.</span><span class="sxs-lookup"><span data-stu-id="71e77-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="71e77-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71e77-110">Examples</span></span>

<span data-ttu-id="71e77-111">O exemplo de JScript a seguir usa a *rede*. **bufferingTime** para especificar o número de segundos alocados para armazenar em buffer os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="71e77-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="71e77-112">As informações são recuperadas de um elemento de entrada de texto HTML criado com ID = "bufText".</span><span class="sxs-lookup"><span data-stu-id="71e77-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="71e77-113">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="71e77-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="71e77-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71e77-114">Requirements</span></span>



| <span data-ttu-id="71e77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e77-115">Requirement</span></span> | <span data-ttu-id="71e77-116">Valor</span><span class="sxs-lookup"><span data-stu-id="71e77-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71e77-117">Versão</span><span class="sxs-lookup"><span data-stu-id="71e77-117">Version</span></span><br/> | <span data-ttu-id="71e77-118">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="71e77-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="71e77-119">DLL</span><span class="sxs-lookup"><span data-stu-id="71e77-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="71e77-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e77-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e77-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="71e77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e77-122">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="71e77-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





