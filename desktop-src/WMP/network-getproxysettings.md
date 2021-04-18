---
title: Método Network. getProxySettings
description: O método getProxySettings recupera a configuração de proxy para um determinado protocolo.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- método getProxySettings Windows Media Player
- método getProxySettings Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751373"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="598b6-106">Método Network. getProxySettings</span><span class="sxs-lookup"><span data-stu-id="598b6-106">Network.getProxySettings method</span></span>

<span data-ttu-id="598b6-107">O método **getProxySettings** recupera a configuração de proxy para um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="598b6-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="598b6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="598b6-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="598b6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="598b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598b6-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="598b6-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598b6-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="598b6-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="598b6-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="598b6-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598b6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="598b6-113">Return value</span></span>

<span data-ttu-id="598b6-114">Esse método retorna um **número** (**Long**) contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="598b6-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="598b6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="598b6-115">Value</span></span> | <span data-ttu-id="598b6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="598b6-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="598b6-117">0</span><span class="sxs-lookup"><span data-stu-id="598b6-117">0</span></span>     | <span data-ttu-id="598b6-118">Um servidor proxy não está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="598b6-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="598b6-119">1</span><span class="sxs-lookup"><span data-stu-id="598b6-119">1</span></span>     | <span data-ttu-id="598b6-120">As configurações de proxy para o navegador atual estão sendo usadas (válida somente para HTTP).</span><span class="sxs-lookup"><span data-stu-id="598b6-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="598b6-121">2</span><span class="sxs-lookup"><span data-stu-id="598b6-121">2</span></span>     | <span data-ttu-id="598b6-122">As configurações de proxy especificadas manualmente estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="598b6-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="598b6-123">3</span><span class="sxs-lookup"><span data-stu-id="598b6-123">3</span></span>     | <span data-ttu-id="598b6-124">As configurações de proxy estão sendo detectadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="598b6-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="598b6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="598b6-125">Remarks</span></span>

<span data-ttu-id="598b6-126">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="598b6-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="598b6-127">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="598b6-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="598b6-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="598b6-128">Examples</span></span>

<span data-ttu-id="598b6-129">O exemplo de JScript a seguir usa a *rede*. **getProxySettings** para exibir uma mensagem, que fornece informações sobre as configurações de proxy atuais do Player, na janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="598b6-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="598b6-130">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="598b6-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="598b6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598b6-131">Requirements</span></span>



| <span data-ttu-id="598b6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="598b6-132">Requirement</span></span> | <span data-ttu-id="598b6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="598b6-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="598b6-134">Versão</span><span class="sxs-lookup"><span data-stu-id="598b6-134">Version</span></span><br/> | <span data-ttu-id="598b6-135">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="598b6-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="598b6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="598b6-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="598b6-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="598b6-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598b6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="598b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598b6-139">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="598b6-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





