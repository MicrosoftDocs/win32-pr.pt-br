---
description: Obtém a chave que é usada para criptografar as mensagens de saída que o token protege.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Método IUpdateEndpointAuthToken:: SigningKey (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010545"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="a3994-103">Método IUpdateEndpointAuthToken:: SigningKey</span><span class="sxs-lookup"><span data-stu-id="a3994-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="a3994-104">Obtém a chave que é usada para criptografar as mensagens de saída que o token protege.</span><span class="sxs-lookup"><span data-stu-id="a3994-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3994-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3994-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="a3994-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3994-107">*pbKey* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a3994-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3994-108">Chave usada para criptografar a mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="a3994-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="a3994-109">*pcbKeySize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a3994-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3994-110">Tamanho da chave referenciada pelo paremeter *pbkey* .</span><span class="sxs-lookup"><span data-stu-id="a3994-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3994-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3994-111">Return value</span></span>

<span data-ttu-id="a3994-112">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a3994-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a3994-113">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3994-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3994-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3994-114">Requirements</span></span>



| <span data-ttu-id="a3994-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3994-115">Requirement</span></span> | <span data-ttu-id="a3994-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a3994-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3994-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3994-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3994-118">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="a3994-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a3994-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3994-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3994-120">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="a3994-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a3994-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3994-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3994-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3994-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3994-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="a3994-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3994-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3994-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a3994-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3994-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3994-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3994-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3994-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a3994-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3994-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3994-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3994-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3994-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3994-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="a3994-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




