---
description: A função EnumMonitors recupera informações sobre os monitores de porta instalados no servidor especificado.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Função EnumMonitors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662122"
---
# <a name="enummonitors-function"></a>Função EnumMonitors

A função **EnumMonitors** recupera informações sobre os monitores de porta instalados no servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os monitores residem. Se esse parâmetro for **nulo**, os monitores locais serão enumerados.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura apontada por *pMonitors*.

Esse valor pode ser 1 ou 2.

</dd> <dt>

*pMonitors* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas. O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres referenciadas pelos membros da estrutura.

Para determinar o tamanho do buffer necessário, chame **EnumMonitors** com *cbBuf* definido como zero. **EnumMonitors** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

O buffer receberá uma matriz de estruturas de [**informações de monitor \_ \_ 1**](monitor-info-1.md) se o *nível* for 1 ou [**monitorará estruturas de \_ informações \_ 2**](monitor-info-2.md) se o *nível* for 2.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pMonitors*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas que foram retornadas no buffer apontado por *pMonitors*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumMonitorsW** (Unicode) e **EnumMonitorsA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informações do MONITOR \_ \_ 1**](monitor-info-1.md)
</dt> <dt>

[**Informações do MONITOR \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

