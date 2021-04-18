---
description: A função ConnectToPrinterDlg exibe uma caixa de diálogo que permite aos usuários navegar e se conectar a impressoras em uma rede.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Função ConnectToPrinterDlg (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810195"
---
# <a name="connecttoprinterdlg-function"></a>Função ConnectToPrinterDlg

A função **ConnectToPrinterDlg** exibe uma caixa de diálogo que permite aos usuários navegar e se conectar a impressoras em uma rede. Se o usuário selecionar uma impressora, a função tentará criar uma conexão a ela; se um driver adequado não estiver instalado no servidor, o usuário terá a opção de criar uma impressora localmente.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Especifica a janela pai da caixa de diálogo.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Esse parâmetro é reservado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido e o usuário selecionar uma impressora, o valor de retorno será um identificador para a impressora selecionada.

Se a função falhar ou o usuário cancelar a caixa de diálogo sem selecionar uma impressora, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A função **ConnectToPrinterDlg** tenta criar uma conexão com a impressora selecionada. No entanto, se o servidor no qual a impressora reside não tiver um driver adequado instalado, a função oferece ao usuário a opção de criar uma impressora localmente. Um aplicativo de chamada pode determinar se a função criou uma impressora localmente chamando [**Getprinter**](getprinter.md) com uma estrutura [**de \_ informações \_ da impressora 2**](printer-info-2.md) e, em seguida, examinando o membro **Attributes** da estrutura.

Um aplicativo deve chamar [**DeletePrinter**](deleteprinter.md) para excluir uma impressora local. Um aplicativo deve chamar [**DeletePrinterConnection**](deleteprinterconnection.md) para excluir uma conexão com uma impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




