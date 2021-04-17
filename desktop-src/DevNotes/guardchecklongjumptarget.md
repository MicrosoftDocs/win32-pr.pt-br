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
# <a name="guardchecklongjumptarget-function"></a>Função GuardCheckLongJumpTarget

## <a name="description"></a>Descrição

Tenta verificar se o destino de um [longjmp](/cpp/c-runtime-library/reference/longjmp) é válido para um processo que tem a [proteção de fluxo de controle (cfg)](../secbp/control-flow-guard.md) habilitada.

Se o endereço de destino corresponder a um mapeamento de imagem, os destinos válidos serão extraídos para o binário.
A função usa esses destinos para validar o destino.
Se o binário não tiver metadados que descrevam o conjunto de destinos de *longjmp* válidos, a função retornará **true**.

Se o endereço de destino corresponder a um mapeamento que não seja de imagem, como no código JIT, uma política global somente leitura será consultada para determinar se o salto é permitido.

## <a name="parameters"></a>Parâmetros

### <a name="targetaddress-in"></a>TargetAddress [in]

O endereço de destino para o salto.

### <a name="flags-in"></a>Flags [in]

Sinalizadores que descrevem a operação a ser executada no endereço.
Se você especificar **GUARD_CHECK_LONGJUMP_NON_FATAL** (0x1), essa função não encerrará o processo se o destino for inválido.

## <a name="returns"></a>Retornos

**True** se o destino for válido, caso contrário, **false**.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também
