---
description: A função CreateNPPInterface usa o BLOB retornado do localizador para criar um NPP que o aplicativo pode usar.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Função CreateNPPInterface (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922008"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="c10a7-103">Função CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="c10a7-103">CreateNPPInterface function</span></span>

<span data-ttu-id="c10a7-104">A função **CreateNPPInterface** usa o blob retornado do localizador para criar um NPP que o aplicativo pode usar.</span><span class="sxs-lookup"><span data-stu-id="c10a7-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c10a7-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="c10a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c10a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c10a7-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c10a7-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c10a7-108">Identificador para o BLOB retornado do localizador.</span><span class="sxs-lookup"><span data-stu-id="c10a7-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="c10a7-109">*IID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="c10a7-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c10a7-110">Identificador da interface que você chama do NPP (**IRTC** ou **IDelaydC**, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="c10a7-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="c10a7-111">*ppvObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c10a7-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c10a7-112">Ponteiro para o ponteiro retornado para a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="c10a7-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c10a7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c10a7-113">Return value</span></span>

<span data-ttu-id="c10a7-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c10a7-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c10a7-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="c10a7-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10a7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c10a7-116">Requirements</span></span>



| <span data-ttu-id="c10a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10a7-117">Requirement</span></span> | <span data-ttu-id="c10a7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c10a7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c10a7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c10a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c10a7-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c10a7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c10a7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c10a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c10a7-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c10a7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c10a7-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c10a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c10a7-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c10a7-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c10a7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c10a7-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c10a7-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c10a7-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c10a7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c10a7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c10a7-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c10a7-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




