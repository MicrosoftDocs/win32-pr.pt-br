---
title: Ocultar evento
description: Ocultar evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822674"
---
# <a name="hide-event"></a>Ocultar evento

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um caractere é ocultado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ ocultar (* *  **ByVal** *characterid*, **ByVal** *causa * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere oculto como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                               |
| *Causa*       | Retorna um valor que indica o que causou a ocultação do caractere. 1 usuário ocultou o caractere selecionando o comando no menu pop-up do ícone da barra de tarefas do caractere ou usando a entrada de fala.<br/> 3 o aplicativo cliente ocultou o caractere.<br/> 5 outro aplicativo cliente ocultou o caractere.<br/> 7 o usuário ocultou o caractere selecionando o comando no menu pop-up do caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor envia esse evento para todos os clientes do caractere. Para consultar o estado atual do caractere, use a propriedade [**Visible**](visible-property.md) .

### <a name="see-also"></a>Consulte Também

[**Mostrar evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





