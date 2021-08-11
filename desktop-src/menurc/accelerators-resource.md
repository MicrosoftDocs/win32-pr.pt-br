---
title: Recurso de ACELERAdores
description: Define um ou mais aceleradores para um aplicativo. Um acelerador é um pressionamento de tecla definido pelo aplicativo para fornecer ao usuário uma maneira rápida de executar uma tarefa.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menus de recursos de ACELERAdores e outros recursos
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ba2d19bbab6346f7a62afe56269f762cd94f7ef1730654fb6ac1abf317e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235735"
---
# <a name="accelerators-resource"></a>Recurso de ACELERAdores

Define um ou mais aceleradores para um aplicativo. Um acelerador é um pressionamento de tecla definido pelo aplicativo para fornecer ao usuário uma maneira rápida de executar uma tarefa.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Zero ou mais das instruções a seguir.



| Instrução                                                        | Descrição                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Características**](characteristics-statement.md) *DWORD*     | Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**características**](characteristics-statement.md). |
| [](language-statement.md) *Idioma* do idioma, *subidioma* | Especifica o idioma do recurso. Para obter mais informações, consulte [**Language**](language-statement.md).                                                                              |
| [](version-statement.md) *DWORD* da versão                     | Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos. Para obter mais informações, consulte [**versão**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*circunstância*
</dt> <dd>

Tecla a ser usada como um acelerador. Pode ser qualquer um dos tipos de caracteres a seguir.



| Type                    | Descrição                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*Char*"                | Um único caractere entre aspas duplas ("). O caractere pode ser precedido por um acento circunflexo (^), o que significa que o caractere é um caractere de controle.                                                                                  |
| *Caractere*             | Um valor inteiro que representa um caractere. O parâmetro de *tipo* deve ser **ASCII**.                                                                                                                                                           |
| *caractere de chave virtual* | Um valor inteiro que representa uma chave virtual. A chave virtual para chaves alfanuméricas pode ser especificada colocando-se a letra maiúscula ou o número entre aspas duplas (por exemplo, "9" ou "C"). O parâmetro de *tipo* deve ser **VIRTKEY**. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

um valor inteiro sem sinal de 16 bits que identifica o acelerador.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*Escreva*
</dt> <dd>

Necessário somente quando o parâmetro de *evento* é um *caractere ou um* caractere de *chave virtual*. O parâmetro de *tipo* especifica **ASCII** ou **VIRTKEY**; o valor inteiro do *evento* é interpretado de acordo. Quando **VIRTKEY** é especificado e o *evento* contém uma cadeia de caracteres, o *evento* deve estar em letras maiúsculas.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Opções*
</dt> <dd>

opções que definem o acelerador. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Opção                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Inverter**                       | Especifica que nenhum item de menu de nível superior é realçado quando o acelerador é usado. Isso é útil ao definir aceleradores para ações como rolagem que não correspondem a um item de menu. Se **Invert** for omitido, um item de menu de nível superior será realçado (se possível) quando o acelerador for usado. Este atributo é obsoleto e mantido somente para compatibilidade com versões anteriores com arquivos de recursos projetados para Windows de 16 bits. |
| **PRESSIONANDO**                            | Faz com que o acelerador seja ativado somente se a tecla ALT estiver inativa. Aplica-se somente a chaves virtuais.                                                                                                                                                                                                                                                                                                                                            |
| **ALTERNÂNCIA**                          | Faz com que o acelerador seja ativado somente se a tecla SHIFT estiver inativa. Aplica-se somente a chaves virtuais                                                                                                                                                                                                                                                                                                                                           |
| [**CONTROLO**](control-control.md) | Define o caractere como um caractere de controle (o acelerador só será ativado se a tecla de controle estiver inoperante). Isso tem o mesmo efeito que usar um acento circunflexo (^) antes do caractere de acelerador no parâmetro de *evento* . Aplica-se somente a chaves virtuais                                                                                                                                                                                           |



 

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

A função [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) é usada para converter mensagens do acelerador da fila do aplicativo no [**\_ comando do WM**](./wm-command.md) ou em mensagens [**\_ SYSCOMMAND do WM**](./wm-syscommand.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso de teclas de aceleração.

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>Veja também

<dl> <dt>

[Usando aceleradores de teclado](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**'**](dialog-resource.md)
</dt> <dt>

[**IDIOMA**](language-statement.md)
</dt> <dt>

[**ADICIONARMENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versão**](version-statement.md)
</dt> </dl>

 

 