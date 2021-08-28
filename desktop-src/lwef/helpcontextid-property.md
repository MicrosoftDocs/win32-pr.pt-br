---
title: Propriedade HelpContextid (objeto de coleção de comandos)
description: Saiba mais sobre a propriedade HelpContextid do objeto da coleção de comandos. o Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0635f62350d0bea31afda09b04e6489fe7f0ccb33173adb6c2aeb69a814265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725696"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Propriedade HelpContextid (objeto de coleção de comandos)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define um número de contexto associado para o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Usado para fornecer ajuda contextual para o objeto **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_"). Comandos ("_*_Name_*_")._ *  \[  =  *Número* de HelpContextID\]



| Parte     | Descrição                                   |
|----------|-----------------------------------------------|
| *Número* | Um inteiro que especifica um número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

se você tiver criado um arquivo de ajuda Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente Help quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário selecionará o objeto [**commands**](/windows/desktop/lwef/the-commands-collection-object) . Se você definir um número de contexto em **HelpContextId**, o Agent chamará ajuda e procurará o tópico identificado por esse número de contexto.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> a criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpFile**](helpfile-property.md)


 

 
