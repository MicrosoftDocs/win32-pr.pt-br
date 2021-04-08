---
description: A função GetProperty retorna um identificador para uma determinada propriedade.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Função GetProperty (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920692"
---
# <a name="getproperty-function"></a><span data-ttu-id="d6f63-103">Função GetProperty</span><span class="sxs-lookup"><span data-stu-id="d6f63-103">GetProperty function</span></span>

<span data-ttu-id="d6f63-104">A função **GetProperty** retorna um identificador para uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="d6f63-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f63-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6f63-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="d6f63-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6f63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f63-107">*hProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f63-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f63-108">Identificador para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="d6f63-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d6f63-109">*PropertyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f63-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f63-110">Nome da propriedade (por exemplo, **soma de verificação**).</span><span class="sxs-lookup"><span data-stu-id="d6f63-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f63-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6f63-111">Return value</span></span>

<span data-ttu-id="d6f63-112">Se a função for bem-sucedida, o valor de retorno será o identificador para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="d6f63-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="d6f63-113">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d6f63-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f63-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f63-114">Remarks</span></span>

<span data-ttu-id="d6f63-115">A função **GetProperty** pode ser usada para obter o identificador de propriedade necessário para localizar instâncias da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d6f63-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="d6f63-116">As funções usadas para localizar as instâncias de propriedade são [FindPropertyInstance](findpropertyinstance.md) (que localiza a primeira instância) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (que localiza a próxima instância).</span><span class="sxs-lookup"><span data-stu-id="d6f63-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="d6f63-117">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetProperty** .</span><span class="sxs-lookup"><span data-stu-id="d6f63-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f63-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f63-118">Requirements</span></span>



| <span data-ttu-id="d6f63-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f63-119">Requirement</span></span> | <span data-ttu-id="d6f63-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f63-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f63-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f63-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f63-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6f63-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d6f63-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f63-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f63-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6f63-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6f63-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d6f63-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f63-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f63-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d6f63-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6f63-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6f63-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6f63-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6f63-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d6f63-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f63-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f63-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f63-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6f63-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f63-132">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="d6f63-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="d6f63-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="d6f63-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




