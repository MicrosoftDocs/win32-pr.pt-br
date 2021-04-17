---
UID: ''
title: Função GuardCheckLongJumpTarget
description: Tenta verificar se o destino de um longjmp é válido.
old-location: ''
ms.assetid: na
ms.date: 04/02/2019
ms.keywords: ''
ms.topic: reference
req.header: guardapiset.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- api-ms-win-core-guard-l1-1-0.dll
api_name:
- GuardCheckLongJumpTarget
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 02f659f77ab2bace129c9b9d9011b4c93e59b2f4
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105756217"
---
# <a name="guardchecklongjumptarget-function"></a><span data-ttu-id="a1504-103">Função GuardCheckLongJumpTarget</span><span class="sxs-lookup"><span data-stu-id="a1504-103">GuardCheckLongJumpTarget function</span></span>

## <a name="description"></a><span data-ttu-id="a1504-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1504-104">Description</span></span>

<span data-ttu-id="a1504-105">Tenta verificar se o destino de um [longjmp](/cpp/c-runtime-library/reference/longjmp) é válido para um processo que tem a [proteção de fluxo de controle (cfg)](../secbp/control-flow-guard.md) habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1504-105">Attempts to verify whether the target of a [longjmp](/cpp/c-runtime-library/reference/longjmp) is valid for a process which has [Control Flow Guard (CFG)](../secbp/control-flow-guard.md) enabled.</span></span>

<span data-ttu-id="a1504-106">Se o endereço de destino corresponder a um mapeamento de imagem, os destinos válidos serão extraídos para o binário.</span><span class="sxs-lookup"><span data-stu-id="a1504-106">If the target address corresponds to an image mapping, the valid targets are extracted for the binary.</span></span>
<span data-ttu-id="a1504-107">A função usa esses destinos para validar o destino.</span><span class="sxs-lookup"><span data-stu-id="a1504-107">The function uses those targets to validate the target.</span></span>
<span data-ttu-id="a1504-108">Se o binário não tiver metadados que descrevam o conjunto de destinos de *longjmp* válidos, a função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="a1504-108">If the binary does not have metadata that describes the set of valid *longjmp* targets, the function returns **TRUE**.</span></span>

<span data-ttu-id="a1504-109">Se o endereço de destino corresponder a um mapeamento que não seja de imagem, como no código JIT, uma política global somente leitura será consultada para determinar se o salto é permitido.</span><span class="sxs-lookup"><span data-stu-id="a1504-109">If the target address corresponds to a non-image mapping, as in JIT code, a global read-only policy is consulted to determine whether the jump is allowed.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1504-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1504-110">Parameters</span></span>

### <a name="targetaddress-in"></a><span data-ttu-id="a1504-111">TargetAddress [in]</span><span class="sxs-lookup"><span data-stu-id="a1504-111">TargetAddress [in]</span></span>

<span data-ttu-id="a1504-112">O endereço de destino para o salto.</span><span class="sxs-lookup"><span data-stu-id="a1504-112">The target address for the jump.</span></span>

### <a name="flags-in"></a><span data-ttu-id="a1504-113">Flags [in]</span><span class="sxs-lookup"><span data-stu-id="a1504-113">Flags [in]</span></span>

<span data-ttu-id="a1504-114">Sinalizadores que descrevem a operação a ser executada no endereço.</span><span class="sxs-lookup"><span data-stu-id="a1504-114">Flags describing the operation to be performed on the address.</span></span>
<span data-ttu-id="a1504-115">Se você especificar **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), essa função não encerrará o processo se o destino for inválido.</span><span class="sxs-lookup"><span data-stu-id="a1504-115">If you specify **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), this function does not terminate the process if the target is invalid.</span></span>

## <a name="returns"></a><span data-ttu-id="a1504-116">Retornos</span><span class="sxs-lookup"><span data-stu-id="a1504-116">Returns</span></span>

<span data-ttu-id="a1504-117">**True** se o destino for válido, caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a1504-117">**TRUE** if the target is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1504-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1504-118">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="a1504-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1504-119">See also</span></span>
