---
title: Método Network. setProxyBypassForLocal
description: O método setProxyBypassForLocal especifica um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- método setProxyBypassForLocal Windows Media Player
- método setProxyBypassForLocal Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811448"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="5a45d-106">Método Network. setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="5a45d-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="5a45d-107">O método **setProxyBypassForLocal** especifica um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="5a45d-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a45d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a45d-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="5a45d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a45d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a45d-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5a45d-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a45d-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="5a45d-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="5a45d-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="5a45d-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a45d-113">*ignorar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a45d-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a45d-114">**Booliano** que especifica se o servidor proxy é ignorado.</span><span class="sxs-lookup"><span data-stu-id="5a45d-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a45d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a45d-115">Return value</span></span>

<span data-ttu-id="5a45d-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5a45d-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a45d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a45d-117">Remarks</span></span>

<span data-ttu-id="5a45d-118">Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="5a45d-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="5a45d-119">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="5a45d-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="5a45d-120">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="5a45d-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5a45d-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a45d-121">Examples</span></span>

<span data-ttu-id="5a45d-122">O exemplo de JScript a seguir usa a *rede*. **setProxyBypassForLocal** para especificar se o servidor proxy do Windows Media Player foi ignorado, ao usar o protocolo MMS, se o servidor de origem estiver em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="5a45d-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="5a45d-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5a45d-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="5a45d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a45d-124">Requirements</span></span>



| <span data-ttu-id="5a45d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a45d-125">Requirement</span></span> | <span data-ttu-id="5a45d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5a45d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a45d-127">Versão</span><span class="sxs-lookup"><span data-stu-id="5a45d-127">Version</span></span><br/> | <span data-ttu-id="5a45d-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5a45d-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5a45d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5a45d-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a45d-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a45d-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a45d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a45d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a45d-132">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="5a45d-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





