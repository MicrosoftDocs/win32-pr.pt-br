---
description: Um tipo de dados usado para especificar os atributos de acesso de segurança no registro.
title: REGSAM (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970830"
---
# <a name="regsam"></a><span data-ttu-id="97417-103">REGSAM</span><span class="sxs-lookup"><span data-stu-id="97417-103">REGSAM</span></span>

<span data-ttu-id="97417-104">Um tipo de dados usado para especificar os atributos de acesso de segurança no registro.</span><span class="sxs-lookup"><span data-stu-id="97417-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="97417-105">Constante</span><span class="sxs-lookup"><span data-stu-id="97417-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="97417-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="97417-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="97417-107"><dt>**CHAVE de \_ todo o \_ acesso**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="97417-108">Combinação de \* \* \* \* valor de consulta de chave \_ \_ \* \* \* \*, \* \* \* \* chave enumerar subchaves \_ \* \* \* \* \_ \_ , \* \* \* \* notificação de chave \* \* \* \*, \* \* \* \* \_ chave \_ criar \_ \_ subchave \* \_ \_ \_ \_ \* \* \*, \* \* \* \* chave de criação de link \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="97417-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="97417-109"><dt>**\_link de criação de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="97417-110">Permissão para criar um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="97417-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="97417-111"><dt>**\_ \_ sub chave de criação de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="97417-112">Permissão para criar subchaves.</span><span class="sxs-lookup"><span data-stu-id="97417-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="97417-113"><dt>**\_sub- \_ \_ chaves enumerar chave**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="97417-114">Permissão para enumerar subchaves.</span><span class="sxs-lookup"><span data-stu-id="97417-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="97417-115"><dt>**\_executar chave**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="97417-116">Permissão para acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="97417-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="97417-117"><dt>**notificação de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="97417-118">Permissão para notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="97417-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="97417-119"><dt>**\_valor da consulta de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="97417-120">Permissão para consultar dados de subchave.</span><span class="sxs-lookup"><span data-stu-id="97417-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="97417-121"><dt>**leitura de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="97417-122">Combinação de \* \* \* \* valor de consulta de chave \_ \_ \* \* \* \*, \* \* \* \* chave enumerar subchaves \_ \* \* \* \* \_ \_ e \* \* \* \* notificação de chave \* \* \* \_ \* acesso.</span><span class="sxs-lookup"><span data-stu-id="97417-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="97417-123"><dt>**\_valor do conjunto de chaves \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="97417-124">Permissão para definir os dados da subchave.</span><span class="sxs-lookup"><span data-stu-id="97417-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="97417-125"><dt>**gravação de chave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97417-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="97417-126">Combinação de \* \* \* \* valor de conjunto de chaves \_ \_ \* \* \* \* e \* \* \* \* chave \_ Create \_ sub \_ Key \* \* \* \* Access.</span><span class="sxs-lookup"><span data-stu-id="97417-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="97417-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="97417-127">Remarks</span></span>

<span data-ttu-id="97417-128">Um valor de **REGSAM** pode ser um ou mais dos valores listados.</span><span class="sxs-lookup"><span data-stu-id="97417-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="97417-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97417-129">Requirements</span></span>



| <span data-ttu-id="97417-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97417-130">Requirement</span></span> | <span data-ttu-id="97417-131">Valor</span><span class="sxs-lookup"><span data-stu-id="97417-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97417-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97417-132">Header</span></span><br/> | <dl> <span data-ttu-id="97417-133"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="97417-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




