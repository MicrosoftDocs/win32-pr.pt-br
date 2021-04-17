---
title: Método Network. getProxyPort
description: O método getProxyPort recupera a porta do proxy que está sendo usada.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- método getProxyPort Windows Media Player
- método getProxyPort Windows Media Player, classe de rede
- Classe de rede Windows Media Player, método getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763030"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="00f8b-106">Método Network. getProxyPort</span><span class="sxs-lookup"><span data-stu-id="00f8b-106">Network.getProxyPort method</span></span>

<span data-ttu-id="00f8b-107">O método **getProxyPort** recupera a porta do proxy que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="00f8b-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f8b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00f8b-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="00f8b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00f8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f8b-110">*protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="00f8b-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f8b-111">**Cadeia de caracteres** que especifica o nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="00f8b-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="00f8b-112">Para obter uma lista de protocolos com suporte, consulte [protocolos e tipos de arquivos com suporte](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="00f8b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f8b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00f8b-113">Return value</span></span>

<span data-ttu-id="00f8b-114">Esse método retorna um **número** (**longo**) que contém a porta do proxy que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="00f8b-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="00f8b-115">O valor retornado é significativo somente quando **getProxySettings** retorna um valor de dois (use configurações manuais).</span><span class="sxs-lookup"><span data-stu-id="00f8b-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="00f8b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="00f8b-116">Remarks</span></span>

<span data-ttu-id="00f8b-117">Esse método falha a menos que o aplicativo de chamada esteja em execução no computador local ou na intranet.</span><span class="sxs-lookup"><span data-stu-id="00f8b-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="00f8b-118">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="00f8b-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="00f8b-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="00f8b-119">Examples</span></span>

<span data-ttu-id="00f8b-120">O exemplo de JScript a seguir usa a *rede*. **getProxyPort** para exibir os números de porta do proxy do Windows Media Player atuais para os protocolos MMS e http.</span><span class="sxs-lookup"><span data-stu-id="00f8b-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="00f8b-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="00f8b-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="00f8b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00f8b-122">Requirements</span></span>



| <span data-ttu-id="00f8b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="00f8b-123">Requirement</span></span> | <span data-ttu-id="00f8b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="00f8b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00f8b-125">Versão</span><span class="sxs-lookup"><span data-stu-id="00f8b-125">Version</span></span><br/> | <span data-ttu-id="00f8b-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="00f8b-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="00f8b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="00f8b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="00f8b-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00f8b-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00f8b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="00f8b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00f8b-130">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="00f8b-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="00f8b-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="00f8b-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





