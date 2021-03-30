---
title: Adicionar método
description: Adicionar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005406"
---
# <a name="add-method"></a>Adicionar método

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Adiciona um objeto de [comando](the-command-object.md) à coleção de [comandos](the-commands-collection-object.md) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Comandos. Adicionar* *  *nome*, *legenda*, *voz*, *habilitado*, *visível*



| Parte      | Descrição                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obrigatórios. Um valor de cadeia de caracteres correspondente à ID que você atribui para o comando.                                                                                                                                                                                                                                        |
| *Legenda* | Opcional. Um valor de cadeia de caracteres correspondente ao nome que aparecerá no menu pop-up do caractere e na janela de comandos quando o aplicativo cliente for de entrada-ativo. Para obter mais informações, consulte a propriedade [Caption](caption-property.md) do objeto [Command](the-command-object.md) .                       |
| *Voz*   | Opcional. Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando. Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a propriedade de [voz](voice-property.md) do objeto de [comando](the-command-object.md) .                                |
| *Enabled* | Opcional. Um valor booliano que indica se o comando está habilitado. O valor padrão é **True**. Para obter mais informações, consulte a propriedade [Enabled](enabled-property.md) do objeto [Command](the-command-object.md) .                                                                                              |
| *Visível* | Opcional. Um valor booliano que indica se o comando está visível no menu pop-up do caractere para o caractere quando o aplicativo cliente é de entrada-ativo. O valor padrão é **True**. Para obter mais informações, consulte a propriedade [visível](visible-property.md) do objeto de [comando](the-command-object.md) . |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor da propriedade [Name](name-property.md) de um objeto de [comando](the-command-object.md) deve ser exclusivo em sua coleção de [comandos](the-commands-collection-object.md) . Você deve remover um comando para poder criar um novo comando com a mesma configuração de propriedade de nome. A tentativa de criar um comando com uma propriedade Name que já existe gera um erro.

Esse método também retorna um objeto de [comando](the-command-object.md) . Isso permite que você declare um objeto e atribua um comando a ele ao chamar o addMethod.


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

 

 




