---
description: A função DocumentProperties recupera ou modifica informações de inicialização de impressora ou exibe uma folha de propriedades de configuração de impressora para a impressora especificada.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Função DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 349a085cc8f55f391b33dd5048d23a35fdac3c2b33b3771290bcecd9fdbcfc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235103"
---
# <a name="documentproperties-function"></a>Função DocumentProperties

A função **DocumentProperties** recupera ou modifica informações de inicialização de impressora ou exibe uma folha de propriedades de configuração de impressora para a impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela pai da folha de propriedades de configuração da impressora.

</dd> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para um objeto de impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pDeviceName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do dispositivo para o qual a folha de propriedades de configuração de impressora é exibida.

</dd> <dt>

*pDevModeOutput* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que recebe os dados de configuração da impressora especificados pelo usuário.

</dd> <dt>

*pDevModeInput* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que o sistema operacional usa para inicializar os controles da folha de propriedades.

Esse parâmetro só será usado se o sinalizador **DM \_ in \_ buffer** estiver definido no parâmetro *fMode* . Se o **DM \_ no \_ buffer** não estiver definido, o sistema operacional usará o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)padrão da impressora.

</dd> <dt>

*fMode* \[ no\]
</dt> <dd>

As operações que a função executa. Se esse parâmetro for zero, a função **DocumentProperties** retornará o número de bytes exigidos pela estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) do driver de impressora. Caso contrário, use uma ou mais das seguintes constantes para construir um valor para esse parâmetro; no entanto, observe que, para alterar as configurações de impressão, um aplicativo deve especificar pelo menos um valor de entrada e um valor de saída.



| Valor                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ no \_ buffer**</dt> </dl>    | Valor de entrada. Antes de solicitar, copiar ou atualizar, a função mescla as configurações de impressão atuais do driver de impressora com as configurações na estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada pelo parâmetro *pDevModeInput* . A função atualiza a estrutura somente para os membros especificados pelo membro **dmFields** da estrutura **DEVMODE** . Esse valor também é definido como **DM \_ Modify**. Em casos de conflito durante a mesclagem, as configurações na estrutura **DEVMODE** especificada por *pDevModeInput* substituem as configurações de impressão atuais do driver de impressora.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ no \_ prompt**</dt> </dl>    | Valor de entrada. A função apresenta a folha de propriedades de configuração de impressão do driver de impressora e, em seguida, altera as configurações na estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) da impressora para esses valores especificados pelo usuário. Esse valor também é definido como **\_ prompt DM**.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**\_buffer de saída DM \_**</dt> </dl> | Valor de saída. A função grava as configurações de impressão atuais do driver de impressora, incluindo dados privados, na estrutura de dados [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada pelo parâmetro *pDevModeOutput* . O chamador deve alocar um buffer suficientemente grande para conter as informações. Se os conjuntos **de \_ \_ buffers de saída** de bit DM estiverem claros, o parâmetro *pDevModeOutput* poderá ser **NULL**. Esse valor também é definido como **\_ cópia DM**.<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o parâmetro *fMode* for zero, o valor de retorno será o tamanho do buffer necessário para conter os dados de inicialização do driver de impressora. Observe que esse buffer pode ser maior do que uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se o driver de impressora acrescentar dados privados à estrutura.

Se a função exibir a folha de propriedades, o valor de retorno será **IDOK** ou **IDCANCEL**, dependendo de qual botão o usuário selecionar.

Se a função não exibir a folha de propriedades e for bem-sucedida, o valor de retorno será **IDOK**.

Se a função falhar, o valor de retorno será menor que zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A cadeia de caracteres apontada pelo parâmetro *pDeviceName* pode ser obtida chamando-se a função [**getprintr**](getprinter.md) .

A estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) realmente usada por um driver de impressora contém a parte independente do dispositivo (conforme definido acima) seguida por uma parte específica do driver que varia em tamanho e conteúdo com cada driver e versão de driver. Devido a essa dependência de driver, é muito importante que os aplicativos consultem o driver para obter o tamanho correto da estrutura **DEVMODE** antes de alocar um buffer para ele.

**Para fazer alterações nas configurações de impressão locais de um aplicativo, um aplicativo deve seguir estas etapas:**

1.  Obtenha o número de bytes necessários para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa chamando **DocumentProperties** e especificando zero no parâmetro *fMode* .
2.  Aloque memória para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.
3.  Obtenha as configurações atuais da impressora chamando **DocumentProperties**. Passe um ponteiro para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) alocada na etapa 2 como o parâmetro *pDevModeOutput* e especifique o valor do **\_ \_ buffer de saída DM** .
4.  Modifique os membros apropriados da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada e indique quais membros foram alterados definindo os bits correspondentes no membro **dmFields** do **DEVMODE**.
5.  Chame **DocumentProperties** e passe a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificada de volta como os parâmetros *pDevModeInput* e *PDevModeOutput* e especifique os valores de buffer **DM \_ no \_ buffer** e **DM \_ out \_** (que são combinados usando o operador OR). A estrutura **DEVMODE** retornada pela terceira chamada para **DocumentProperties** pode ser usada como um argumento em uma chamada para a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .

Para criar um identificador para um contexto de dispositivo de impressora usando as configurações de impressora atuais, você só precisa chamar **DocumentProperties** duas vezes, conforme descrito acima. A primeira chamada Obtém o tamanho do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo e a segunda chamada Inicializa o **DEVMODE** com as configurações de impressora atuais. Passe o **DEVMODE** inicializado para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) para obter o identificador para o contexto do dispositivo de impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **DocumentPropertiesW** (Unicode) e **DocumentPropertiesA** (ANSI)<br/>                           |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

