---
title: Método Network. setProxyPort
description: O método setProxyPort especifica a porta proxy a ser usada. | Método Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- método setProxyPort Windows Media Player
- método setProxyPort Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794616"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="1cd7f-107">Método Network. setProxyPort</span><span class="sxs-lookup"><span data-stu-id="1cd7f-107">Network.setProxyPort method</span></span>

<span data-ttu-id="1cd7f-108">O método **setProxyPort** especifica a porta proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd7f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cd7f-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="1cd7f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cd7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd7f-111">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1cd7f-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd7f-112">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="1cd7f-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1cd7f-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cd7f-114">*porta* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1cd7f-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd7f-115">**Número** (**longo**) que especifica a porta do proxy a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd7f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cd7f-116">Return value</span></span>

<span data-ttu-id="1cd7f-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd7f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cd7f-118">Remarks</span></span>

<span data-ttu-id="1cd7f-119">Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="1cd7f-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="1cd7f-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="1cd7f-121">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1cd7f-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1cd7f-122">Examples</span></span>

<span data-ttu-id="1cd7f-123">O exemplo de JScript a seguir usa a *rede*. **setProxyPort** para especificar o número da porta do proxy do Windows Media Player para o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="1cd7f-124">O número da porta é recuperado de um elemento de entrada HTML com ID = "PORT".</span><span class="sxs-lookup"><span data-stu-id="1cd7f-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="1cd7f-125">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1cd7f-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="1cd7f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cd7f-126">Requirements</span></span>



| <span data-ttu-id="1cd7f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cd7f-127">Requirement</span></span> | <span data-ttu-id="1cd7f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1cd7f-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd7f-129">Versão</span><span class="sxs-lookup"><span data-stu-id="1cd7f-129">Version</span></span><br/> | <span data-ttu-id="1cd7f-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1cd7f-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1cd7f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd7f-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cd7f-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd7f-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cd7f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cd7f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd7f-134">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="1cd7f-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





