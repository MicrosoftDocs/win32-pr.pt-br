---
description: A função addmonitor instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Função addmonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011734"
---
# <a name="addmonitor-function"></a>Função addmonitor

A função **addmonitor** instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o monitor deve ser instalado. Para sistemas que dão suporte apenas à instalação local de monitores, essa cadeia de caracteres deve ser **nula**.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pMonitors* aponta. Esse valor deve ser 2.

</dd> <dt>

*pMonitors* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**informações do monitor \_ \_ 2**](monitor-info-2.md) . Se o membro **pEnvironment** da estrutura *pMonitors* for **NULL**, o ambiente atual do chamador (cliente), não do destino (servidor), será usado.

Observe que a chamada falhará se o ambiente não corresponder ao ambiente do servidor, ou seja, você só poderá adicionar um monitor que foi gravado para a arquitetura do servidor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes que um aplicativo chame a função **addmonitor** , todos os arquivos exigidos pelo monitor devem ser copiados para o diretório system32.

Para determinar os monitores de porta que estão instalados no momento, chame a função [**EnumMonitors**](enummonitors.md) .

Para remover um monitor adicionado por **addmonitor**, chame a função [**DeleteMonitor**](deletemonitor.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddMonitorW** (Unicode) e **addmonitora** (ANSI)<br/>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeleteMonitor**](deletemonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Informações do MONITOR \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

