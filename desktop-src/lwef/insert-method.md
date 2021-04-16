---
title: Método Insert
description: Método Insert
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105779337"
---
# <a name="insert-method"></a>Método Insert

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Insere um objeto de **comando** na coleção de **comandos** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Comandos. Insert* *  *nome*, *refname*, *antes*\_

*Legenda*, *voz, habilitada, visível*



| Parte      | Descrição                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obrigatórios. Um valor de cadeia de caracteres correspondente à ID que você atribui ao [**comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *RefName* | Obrigatórios. Um valor de cadeia de caracteres correspondente ao nome (ID) do comando logo acima ou abaixo do local em que você deseja inserir o novo comando.                                                                                                                                                                 |
| *Antes*  | Opcional. Um valor booliano que indica se o comando novo deve ser inserido antes do comando especificado por *refname*. **True** (padrão). O novo comando será inserido antes do comando referenciado.<br/> **Falso** O novo comando será inserido após o comando referenciado.<br/> |
| *Legenda* | Opcional. Um valor de cadeia de caracteres correspondente ao nome que aparecerá no menu pop-up do caractere e na janela de comandos quando o aplicativo cliente for de entrada-ativo. Para obter mais informações, consulte a propriedade [**Caption**](caption-property.md)do objeto [**Command**](/windows/desktop/lwef/the-command-object) .    |
| *Voz*   | Opcional. Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando. Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a propriedade de **voz** do objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                                  |
| *Enabled* | Opcional. Um valor booliano que indica se o comando está habilitado. O valor padrão é **True**. Para obter mais informações, consulte a propriedade **Enabled** do objeto [**Command**](/windows/desktop/lwef/the-command-object) .                                                                                                  |
| *Visível* | Opcional. Um valor booliano que indica se o comando está visível na janela de comandos quando o aplicativo cliente é de entrada-ativo. O valor padrão é **True**. Para obter mais informações, consulte a propriedade [**visível**](visible-property.md) do objeto de [**comando**](/windows/desktop/lwef/the-command-object) .       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor da propriedade [**Name**](name-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) deve ser exclusivo em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Você deve remover um **comando** para poder criar um novo **comando** com a mesma configuração de propriedade de **nome** . A tentativa de criar um **comando** com uma propriedade **Name** que já existe gera um erro.

Esse método também retorna um objeto de [**comando**](/windows/desktop/lwef/the-command-object) . Isso permite que você declare um objeto e atribua um **comando** a ele ao chamar o método **Insert** .


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Consulte Também

Método [**Add**](add-method.md), método [**Remove**](remove-method.md), [**método RemoveAll**](removeall-method.md)


 

