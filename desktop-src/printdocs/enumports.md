---
description: A função EnumPorts enumera as portas disponíveis para impressão em um servidor especificado.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Função EnumPorts (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d1f5abc20e94c53e005ee97727a7de789f172bfef1d66703c72690910f197f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056401"
---
# <a name="enumports-function"></a>Função EnumPorts

A **função EnumPorts** enumera as portas disponíveis para impressão em um servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor cujas portas de impressora você deseja enumerar.

Se *pName* for **NULL,** a função enumera as portas de impressora do computador local.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O tipo de informações retornadas no buffer *pPorts.* Se *Level* for 1, *pPorts* receberá uma matriz de estruturas [**PORT INFO \_ \_ 1.**](port-info-1.md) Se *Level* for 2, *pPorts* receberá uma matriz de estruturas [**PORT INFO \_ \_ 2.**](port-info-2.md)

</dd> <dt>

*pPorts* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas [**PORT \_ INFO \_ 1**](port-info-1.md) ou [**PORT INFO \_ \_ 2.**](port-info-2.md) Cada estrutura contém dados que descrevem uma porta de impressora disponível. O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.

Para determinar o tamanho do buffer necessário, chame **EnumPorts** com *cbBuf* definido como zero. **EnumPorts** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna ERROR INSUFFICIENT BUFFER e o parâmetro \_ \_ *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPorts*.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pPorts.* Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas [**PORT \_ INFO \_ 1**](port-info-1.md) ou [**PORT INFO \_ \_ 2**](port-info-2.md) retornadas no buffer *pPorts.* Esse é o número de portas de impressora disponíveis no servidor especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A **função EnumPorts** poderá ser bem-sucedida mesmo que o servidor especificado por *pName* não tenha uma impressora definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPortsW** (Unicode) **e EnumPortsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA PORTA \_ 1**](port-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA PORTA \_ 2**](port-info-2.md)
</dt> </dl>

 

