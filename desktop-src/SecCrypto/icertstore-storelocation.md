---
description: Define ou recupera o \_ local de armazenamento CApicor \_ de um repositório de certificados.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Propriedade ICertStore:: StoreLocation'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769281"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="e22a3-103">Propriedade ICertStore:: StoreLocation</span><span class="sxs-lookup"><span data-stu-id="e22a3-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="e22a3-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="e22a3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="e22a3-105">A propriedade **StoreLocation** define ou recupera o [**\_ \_ local de armazenamento capicor**](capicom-store-location.md) de um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="e22a3-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="e22a3-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e22a3-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e22a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e22a3-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="e22a3-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e22a3-108">Property value</span></span>

<span data-ttu-id="e22a3-109">O local do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="e22a3-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e22a3-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e22a3-110">Error codes</span></span>

<span data-ttu-id="e22a3-111">Se os métodos de acesso à propriedade **colocarem \_ StoreLocation** e o **\_ StoreLocation** forem bem-sucedidos, eles retornarão S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e22a3-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="e22a3-112">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="e22a3-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e22a3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e22a3-113">Requirements</span></span>



| <span data-ttu-id="e22a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e22a3-114">Requirement</span></span> | <span data-ttu-id="e22a3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e22a3-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e22a3-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e22a3-116">Redistributable</span></span><br/> | <span data-ttu-id="e22a3-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e22a3-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e22a3-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e22a3-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="e22a3-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e22a3-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22a3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e22a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22a3-121">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="e22a3-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




