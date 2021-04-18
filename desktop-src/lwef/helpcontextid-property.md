---
title: Propriedade HelpContextid (objeto de coleção de comandos)
description: Propriedade HelpContextid
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454548"
---
# <a name="helpcontextid-property-commands-collection-object"></a>Propriedade HelpContextid (objeto de coleção de comandos)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionará o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Se você definir um número de contexto em **HelpContextId**, o Agent chamará ajuda e procurará o tópico identificado por esse número de contexto.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpFile**](helpfile-property.md)


 

 
