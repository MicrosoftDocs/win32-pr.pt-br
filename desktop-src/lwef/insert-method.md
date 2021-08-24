---
title: Método Insert
description: Método Insert
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94b63da0477ee048239afa34ff57475dcce8f0d1129f4574d6b7b6543d75e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114626"
---
# <a name="insert-method"></a>Método Insert

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Insere **um objeto Command** na coleção **Comandos.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Insert_ *  *Name*, *RefName*, *Before*\_

*Legenda ,* *Voz, Habilitado, Visível*



| Parte      | Descrição                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obrigatórios. Um valor de cadeia de caracteres correspondente à ID que você atribui ao [**Comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *Refname* | Obrigatórios. Um valor de cadeia de caracteres correspondente ao nome (ID) do comando logo acima ou abaixo em que você deseja inserir o novo comando.                                                                                                                                                                 |
| *Antes*  | Opcional. Um valor booliana que indica se o novo comando deve ser inserido antes do comando especificado por *RefName.* **True** (padrão). O novo comando será inserido antes do comando referenciado.<br/> **False** O novo comando será inserido após o comando referenciado.<br/> |
| *Legenda* | Opcional. Um valor de cadeia de caracteres correspondente ao nome que será exibido no menu pop-up do caractere e na Janela Comandos quando o aplicativo cliente estiver ativo de entrada. Para obter mais informações, consulte [**a propriedade Legenda**](/windows/desktop/lwef/the-command-object) do objeto [**Command.**](caption-property.md)    |
| *Voz*   | Opcional. Um valor de cadeia de caracteres correspondente às palavras ou frases a serem usadas pelo mecanismo de fala para reconhecer esse comando. Para obter mais informações sobre como formatar alternativas para a cadeia de caracteres, consulte a [**propriedade**](/windows/desktop/lwef/the-command-object) Voz do **objeto Command.**                                  |
| *Habilitada* | Opcional. Um valor booliana que indica se o comando está habilitado. O valor padrão é **True**. Para obter mais informações, consulte [**a propriedade Enabled**](/windows/desktop/lwef/the-command-object) **do objeto** Command.                                                                                                  |
| *Visível* | Opcional. Um valor booliana que indica se o comando está visível na janela Comandos quando o aplicativo cliente está ativo de entrada. O valor padrão é **True**. Para obter mais informações, consulte [**a propriedade**](/windows/desktop/lwef/the-command-object) Visible do [**objeto Command.**](visible-property.md)       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor da propriedade [**Nome**](/windows/desktop/lwef/the-command-object) de um objeto [**Command**](name-property.md) deve ser exclusivo em sua [**coleção De**](/windows/desktop/lwef/the-commands-collection-object) comandos. Você deve remover um **Comando antes** de criar um novo **Comando com** a mesma **configuração de propriedade** Name. Tentar criar um **Comando com** uma **propriedade Name** que já existe gera um erro.

Esse método também retorna um [**objeto Command.**](/windows/desktop/lwef/the-command-object) Isso permite que você declare um objeto e atribua um **Comando** a ele ao chamar o **método Insert.**


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Consulte Também

[**Método Add**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)


 

