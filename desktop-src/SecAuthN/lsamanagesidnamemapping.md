---
UID: ''
title: Função LsaManageSidNameMapping
description: Adiciona ou remove mapeamentos de SID/nome do conjunto de mapeamento registrado com o serviço de pesquisa do LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 6c2a66a318076588b725f74e9f03a23b8a134595b196dbf140850e72a7d78d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921855"
---
# <a name="lsamanagesidnamemapping-function"></a>Função LsaManageSidNameMapping

## <a name="description"></a>Description

A função **LsaManageSidNameMapping** adiciona ou remove mapeamentos de Sid/nome do conjunto de mapeamento registrado com o serviço de pesquisa do LSA.

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>Parâmetros

### <a name="optype-in"></a>OpType [in]

Indica se uma função this está sendo chamada para adicionar ou remover um mapeamento de SID/nome.

### <a name="opinput-in"></a>OpInput [in]

Indica o domínio, a conta e os valores de SID a serem usados durante esta operação. Sinalizadores adicionais também podem ser definidos nessa estrutura.

### <a name="opoutput-out"></a>OpOutput [saída]

Contém um valor de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) que indica êxito ou falha na operação.

| Valor | Significado |
|-------|---------|
| **Êxito** | A operação foi concluída sem erro. |
| **NonMappingError** | Ocorreu um erro não relacionado ao mapeamento de nome de SID. |
| **NameCollision** | Falha na operação devido à colisão de nome. |
| **SidCollision** | Falha na operação devido à colisão de SID. |
| **DomainNotFound (Domínio não encontrado)** | Domínio correspondente não encontrado. |
| **DomainSidPrefixMismatch** | O SID fornecido não tem o prefixo de domínio correto. |
| **MappingNotFound** | Mapeamento não encontrado no cache. |

## <a name="returns"></a>Retornos

Se o mapeamento for inserido com êxito, o valor de retorno será STATUS_SUCCESS.
Caso contrário, se a função falhar devido a conflitos de SID ou de nome, STATUS_INVALID_PARAMETER erro será retornado.

## <a name="remarks"></a>Comentários

## <a name="see-also"></a>Confira também
