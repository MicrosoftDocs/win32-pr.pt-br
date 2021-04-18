---
title: Método Network. setproxyname
description: O método setproxyname especifica o nome do servidor proxy a ser usado. | Método Network. setproxyname
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- método setproxyname do Windows Media Player
- método setproxyname Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método setproxyname
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788885"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="c56bf-107">Método Network. setproxyname</span><span class="sxs-lookup"><span data-stu-id="c56bf-107">Network.setProxyName method</span></span>

<span data-ttu-id="c56bf-108">O método **Setproxyname** especifica o nome do servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c56bf-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56bf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c56bf-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="c56bf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c56bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56bf-111">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c56bf-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56bf-112">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="c56bf-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="c56bf-113">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c56bf-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56bf-114">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c56bf-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56bf-115">**Cadeia de caracteres** que especifica o nome do servidor proxy a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c56bf-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56bf-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c56bf-116">Return value</span></span>

<span data-ttu-id="c56bf-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c56bf-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56bf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c56bf-118">Remarks</span></span>

<span data-ttu-id="c56bf-119">Esse método não tem efeito, a menos que **getProxySettings** retorne um valor de 2 (use as configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="c56bf-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="c56bf-120">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="c56bf-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="c56bf-121">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="c56bf-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c56bf-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c56bf-122">Examples</span></span>

<span data-ttu-id="c56bf-123">O exemplo de JScript a seguir usa a *rede*. **Setproxyname** para especificar o nome do servidor proxy do Windows Media Player para o protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="c56bf-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="c56bf-124">O novo nome é recuperado de um elemento de texto HTML com ID = "NAME".</span><span class="sxs-lookup"><span data-stu-id="c56bf-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="c56bf-125">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c56bf-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="c56bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56bf-126">Requirements</span></span>



| <span data-ttu-id="c56bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56bf-127">Requirement</span></span> | <span data-ttu-id="c56bf-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c56bf-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c56bf-129">Versão</span><span class="sxs-lookup"><span data-stu-id="c56bf-129">Version</span></span><br/> | <span data-ttu-id="c56bf-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c56bf-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c56bf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c56bf-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="c56bf-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56bf-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56bf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c56bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56bf-134">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="c56bf-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





