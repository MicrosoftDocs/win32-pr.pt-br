---
description: A função ConfigurePort exibe a caixa de diálogo porta-configuração de uma porta no servidor especificado.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Função ConfigurePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921684"
---
# <a name="configureport-function"></a>Função ConfigurePort

A função **ConfigurePort** exibe a caixa de diálogo porta-configuração de uma porta no servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual a porta especificada existe. Se esse parâmetro for **NULL**, a porta será local.

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Identificador para a janela pai da caixa de diálogo porta-configuração.

</dd> <dt>

*pPortName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da porta a ser configurada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Antes de chamar a função **ConfigurePort** , um aplicativo deve chamar a função [**EnumPorts**](enumports.md) para determinar nomes de porta válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **ConfigurePortW** (Unicode) e **ConfigurePortA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




