---
description: Define ou recupera o identificador HCERTSTORE de um repositório de certificados.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Propriedade ICertStore:: StoreHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779362"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="08792-103">Propriedade ICertStore:: StoreHandle</span><span class="sxs-lookup"><span data-stu-id="08792-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="08792-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="08792-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="08792-105">A propriedade **StoreHandle** define ou recupera o identificador HCERTSTORE de um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="08792-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="08792-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="08792-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="08792-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08792-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="08792-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="08792-108">Property value</span></span>

<span data-ttu-id="08792-109">O identificador HCERTSTORE do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="08792-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08792-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="08792-110">Error codes</span></span>

<span data-ttu-id="08792-111">Se os métodos de acesso à propriedade **colocarem \_ StoreHandle** e o **\_ StoreHandle** forem bem-sucedidos, eles retornarão S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08792-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="08792-112">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="08792-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="08792-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="08792-113">Remarks</span></span>

<span data-ttu-id="08792-114">Você deve chamar o método [**CloseHandle**](icertstore-closehandle.md) ou a função [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) para liberar o contexto.</span><span class="sxs-lookup"><span data-stu-id="08792-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="08792-115">Se você definir a propriedade **StoreHandle** , o estado do objeto de [**loja**](store.md) inteiro será redefinido.</span><span class="sxs-lookup"><span data-stu-id="08792-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="08792-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08792-116">Requirements</span></span>



| <span data-ttu-id="08792-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08792-117">Requirement</span></span> | <span data-ttu-id="08792-118">Valor</span><span class="sxs-lookup"><span data-stu-id="08792-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08792-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="08792-119">Redistributable</span></span><br/> | <span data-ttu-id="08792-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="08792-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08792-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08792-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="08792-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08792-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08792-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="08792-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08792-124">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="08792-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




