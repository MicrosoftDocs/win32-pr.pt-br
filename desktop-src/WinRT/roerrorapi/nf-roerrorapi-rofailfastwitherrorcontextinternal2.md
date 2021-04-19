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
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105780749"
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

Uma matriz de ponteiros para [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) estruturas. Cada estrutura contém informações que descrevem uma exceção dedevida. As informações nessas estruturas são enviadas para Relatório de Erros do Windows (WER) junto com as informações de exceção decorrida que foram capturadas pela plataforma.

## <a name="return-value"></a>Retornar valor

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