---
title: Função RoFailFastWithErrorContextInternal2
description: Gera uma exceção não continuável no processo atual e também permite que você inclua o contexto de erro adicional ainda não capturado pelo sistema operacional.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: a2e8e2e357b7c4768596ca36cb48cdf1bb2cfdbd839ecc6949a607975d6000c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560622"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>Função RoFailFastWithErrorContextInternal2

Gera uma exceção não continuável no processo atual e também permite que você inclua o contexto de erro adicional ainda não capturado pelo sistema operacional (SO).

## <a name="syntax"></a>Sintaxe

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>Parâmetros

`hrError`

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

O **HRESULT** associado ao erro atual. A exceção é gerada para qualquer valor de *hrError*.

`cStowedExceptions`

Tipo: **[ULONG](../../winprog/windows-data-types.md)**

O número de elementos na matriz *aStowedExceptionPointers* .

`aStowedExceptionPointers`

Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

Uma matriz de ponteiros para [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) estruturas. Cada estrutura contém informações que descrevem uma exceção dedevida. as informações nessas estruturas são enviadas para Relatório de Erros do Windows (WER) junto com as informações de exceção decorrida que foram capturadas pela plataforma.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

**RoFailFastWithErrorContextInternal2** não está associado a uma biblioteca de importação nem a um arquivo de cabeçalho. Você pode chamá-lo primeiro usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (para carregar `ComBase.dll` ) e, em seguida, chamando a função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar o endereço de **RoFailFastWithErrorContextInternal2**.

Para obter mais informações, consulte a [função RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de Destino** | Windows |
| **Cabeçalho** | N/D |
| **Biblioteca** | N/D |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>Confira também

* [Função RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)