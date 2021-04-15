---
description: Recupera o tipo de MAC da categoria NetworkInfo da seção NPP do BLOB e converte os dados de tipo em um número de tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Função GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501349"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="7ce0a-103">Função GetNPPMacTypeAsNumber</span><span class="sxs-lookup"><span data-stu-id="7ce0a-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="7ce0a-104">A função **GetNPPMacTypeAsNumber** recupera o tipo de Mac da categoria NetworkInfo da seção NPP do blob e converte os dados de tipo em um número de tipo Mac.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ce0a-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="7ce0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ce0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce0a-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ce0a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce0a-108">Um identificador para o BLOB especificado.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="7ce0a-109">*lpMacType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7ce0a-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce0a-110">Um ponteiro para o tipo de MAC.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce0a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ce0a-111">Return value</span></span>

<span data-ttu-id="7ce0a-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7ce0a-113">Se a marca não estiver disponível, o valor de retorno será \_ tipo de Mac \_ desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ce0a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ce0a-114">Remarks</span></span>

<span data-ttu-id="7ce0a-115">Essa função mapeia a marca, **NPP: NetworkInfo: MacType** para o **\_ \_ \* tipo de Mac** , conforme definido no arquivo Npptypes. h.</span><span class="sxs-lookup"><span data-stu-id="7ce0a-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce0a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce0a-116">Requirements</span></span>



| <span data-ttu-id="7ce0a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce0a-117">Requirement</span></span> | <span data-ttu-id="7ce0a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7ce0a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce0a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ce0a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce0a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ce0a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7ce0a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ce0a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce0a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ce0a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ce0a-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7ce0a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ce0a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce0a-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="7ce0a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ce0a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ce0a-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ce0a-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ce0a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ce0a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce0a-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce0a-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




