---
description: A função AddPort adiciona o nome de uma porta à lista de portas com suporte. A função AddPort é exportada pelo monitor de porta.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Função AddPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837052"
---
# <a name="addport-function"></a>Função AddPort

A função **AddPort** adiciona o nome de uma porta à lista de portas com suporte. A função **AddPort** é exportada pelo monitor de porta.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome do servidor ao qual a porta está conectada. Se esse parâmetro for **NULL**, a porta será local.

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela pai da caixa de diálogo **AddPort** .

</dd> <dt>

*pMonitorName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o monitor associado à porta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A função **AddPort** procura a rede para localizar as portas existentes e exibe uma caixa de diálogo para o usuário. A função **AddPort** deve validar o nome da porta inserido pelo usuário chamando [**EnumPorts**](enumports.md) para garantir que não existam nomes duplicados.

O chamador da função **AddPort** deve ter acesso ao servidor para \_ \_ administrar o acesso ao servidor ao qual a porta está conectada.

Para adicionar uma porta sem exibir uma caixa de diálogo, chame a função **XcvData** em vez de **AddPort**. Para obter mais informações sobre o **XcvData**, consulte o Microsoft Windows Driver Development Kit (DDK).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **AddPortW** (Unicode) e **addportaa** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




