---
title: Método Network. setProxySettings
description: O método setProxySettings especifica a configuração de proxy para um determinado protocolo.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- método setProxySettings Windows Media Player
- método setProxySettings Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763205"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="cf0f8-106">Método Network. setProxySettings</span><span class="sxs-lookup"><span data-stu-id="cf0f8-106">Network.setProxySettings method</span></span>

<span data-ttu-id="cf0f8-107">O método **setProxySettings** especifica a configuração de proxy para um determinado protocolo.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0f8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf0f8-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="cf0f8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf0f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0f8-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cf0f8-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0f8-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="cf0f8-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="cf0f8-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf0f8-113">*configuração* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cf0f8-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0f8-114">**Número** (**longo**) que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="cf0f8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0f8-115">Value</span></span> | <span data-ttu-id="cf0f8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf0f8-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="cf0f8-117">0</span><span class="sxs-lookup"><span data-stu-id="cf0f8-117">0</span></span>     | <span data-ttu-id="cf0f8-118">Não use um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="cf0f8-119">1</span><span class="sxs-lookup"><span data-stu-id="cf0f8-119">1</span></span>     | <span data-ttu-id="cf0f8-120">Use as configurações de proxy do navegador atual (válido somente para HTTP).</span><span class="sxs-lookup"><span data-stu-id="cf0f8-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="cf0f8-121">2</span><span class="sxs-lookup"><span data-stu-id="cf0f8-121">2</span></span>     | <span data-ttu-id="cf0f8-122">Use as configurações de proxy especificadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="cf0f8-123">3</span><span class="sxs-lookup"><span data-stu-id="cf0f8-123">3</span></span>     | <span data-ttu-id="cf0f8-124">Detectar automaticamente as configurações de proxy.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0f8-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf0f8-125">Return value</span></span>

<span data-ttu-id="cf0f8-126">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf0f8-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf0f8-127">Remarks</span></span>

<span data-ttu-id="cf0f8-128">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="cf0f8-129">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="cf0f8-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cf0f8-130">Examples</span></span>

<span data-ttu-id="cf0f8-131">O exemplo a seguir usa JScript com um elemento HTML SELECT **para permitir que o usuário especifique a configuração de proxy do Windows Media Player para o protocolo http. O objeto de jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cf0f8-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="cf0f8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf0f8-132">Requirements</span></span>



| <span data-ttu-id="cf0f8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf0f8-133">Requirement</span></span> | <span data-ttu-id="cf0f8-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0f8-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0f8-135">Versão</span><span class="sxs-lookup"><span data-stu-id="cf0f8-135">Version</span></span><br/> | <span data-ttu-id="cf0f8-136">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cf0f8-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cf0f8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf0f8-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf0f8-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf0f8-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf0f8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf0f8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0f8-140">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="cf0f8-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





