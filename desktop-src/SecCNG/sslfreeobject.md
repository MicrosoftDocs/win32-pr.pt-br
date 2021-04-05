---
description: Libera um objeto de chave, hash ou provedor.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Função SslFreeObject (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827934"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="311b4-103">Função SslFreeObject</span><span class="sxs-lookup"><span data-stu-id="311b4-103">SslFreeObject function</span></span>

<span data-ttu-id="311b4-104">A função **SslFreeObject** libera um objeto de chave, hash ou provedor.</span><span class="sxs-lookup"><span data-stu-id="311b4-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="311b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="311b4-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="311b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="311b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311b4-107">*hObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="311b4-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311b4-108">O identificador do objeto a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="311b4-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="311b4-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="311b4-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311b4-110">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="311b4-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311b4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="311b4-111">Return value</span></span>

<span data-ttu-id="311b4-112">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="311b4-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="311b4-113">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="311b4-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="311b4-114">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="311b4-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="311b4-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="311b4-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="311b4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="311b4-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="311b4-117"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="311b4-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="311b4-118">Um identificador interno não é válido.</span><span class="sxs-lookup"><span data-stu-id="311b4-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="311b4-119"><dt>**Status \_ do \_Identificador inválido**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="311b4-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="311b4-120">O identificador fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="311b4-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="311b4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="311b4-121">Requirements</span></span>



| <span data-ttu-id="311b4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="311b4-122">Requirement</span></span> | <span data-ttu-id="311b4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="311b4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="311b4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="311b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="311b4-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="311b4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="311b4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="311b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="311b4-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="311b4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="311b4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="311b4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="311b4-129"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="311b4-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="311b4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="311b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="311b4-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="311b4-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




