---
title: Propriedade GlobalVoiceCommandsEnabled
description: Propriedade GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f889d242afca406ba443fd3d9a19afb837fbed0390f5c0c3d2bbd2ac2ccbccb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751440"
---
# <a name="globalvoicecommandsenabled-property"></a>Propriedade GlobalVoiceCommandsEnabled

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se a voz está habilitada para os comandos globais do agente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*caracteres Agent. ***("**_characterid_*_"). Commands. GlobalVoiceCommandsEnabled_*

\[ = *Boolean*\]



| Parte      | Descrição                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que indica se os parâmetros de voz para comandos globais do agente estão habilitados. Os parâmetros de voz **verdadeiros** (padrão) estão habilitados. <br/> **Falso** Os parâmetros de voz estão desabilitados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere. Se você definir **GlobalVoiceCommandsEnabled** como **false**, o Agent desabilitará quaisquer parâmetros de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de outros [**comandos**](/windows/desktop/lwef/the-commands-collection-object) do cliente. Isso permite que você os elimine da gramática ativa atual do seu cliente. No entanto, como isso potencialmente bloqueia o acesso de voz a outros clientes, redefina essa propriedade como **true** depois de processar a entrada de voz do usuário.

Desabilitar a propriedade não afeta o menu pop-up do caractere. Os comandos globais adicionados pelo servidor ainda serão exibidos. Você não pode removê-los do menu pop-up.

 

