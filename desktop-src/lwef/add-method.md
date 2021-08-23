---
title: Adicionar método
description: Adicionar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ae6cc3cd0a39be8b293a6ae64a96859e5d4fcf6d23ff410439422676b3527e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976826"
---
# <a name="add-method"></a>Adicionar método

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Adiciona um [objeto Command](the-command-object.md) à [coleção Comandos.](the-commands-collection-object.md)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Add_ *  *Name*, *Caption*, *Voice*, *Enabled*, *Visible*



| Parte      | Descrição                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obrigatórios. Um valor de cadeia de caracteres correspondente à ID que você atribui para o comando.                                                                                                                                                                                                                                        |
| *Legenda* | Opcional. Um valor de cadeia de caracteres correspondente ao nome que será exibido no menu pop-up do caractere e na Janela Comandos quando o aplicativo cliente estiver ativo de entrada. Para obter mais informações, consulte [a propriedade Legenda](the-command-object.md) do objeto [Command.](caption-property.md)                       |
| *Voz*   | Opcional. Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando. Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a [propriedade](the-command-object.md) Voz do [objeto Command.](voice-property.md)                                |
| *Habilitada* | Opcional. Um valor booliana que indica se o comando está habilitado. O valor padrão é **True**. Para obter mais informações, consulte [a propriedade Enabled](the-command-object.md) [do objeto](enabled-property.md) Command.                                                                                              |
| *Visível* | Opcional. Um valor booliana que indica se o comando está visível no menu pop-up do caractere para o caractere quando o aplicativo cliente está ativo de entrada. O valor padrão é **True**. Para obter mais informações, consulte [a propriedade](the-command-object.md) Visible do [objeto Command.](visible-property.md) |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor da propriedade [Nome](the-command-object.md) de um objeto [Command](name-property.md) deve ser exclusivo em sua [coleção De](the-commands-collection-object.md) comandos. Você deve remover um Comando antes de criar um novo Comando com a mesma configuração de propriedade Name. Tentar criar um Comando com uma propriedade Name que já existe gera um erro.

Esse método também retorna um [objeto Command.](the-command-object.md) Isso permite que você declare um objeto e atribua um Comando a ele ao chamar o Addmethod.


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Método insert**](insert-method.md)
</dt> <dt>

[**Método RemoveAll**](removeall-method.md)
</dt> <dt>

[**Remover método**](remove-method.md)
</dt> </dl>

 

 




