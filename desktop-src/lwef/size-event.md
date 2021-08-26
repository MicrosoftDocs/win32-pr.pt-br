---
title: Evento de tamanho
description: Evento de tamanho
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961016"
---
# <a name="size-event"></a>Evento de tamanho

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o tamanho de um caractere é alterado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 Tamanho do *subagente* \_ **(ByVal** *caractereid*, **ByVal** *largura*, **ByVal** *Height*)



| Parte          | Descrição                                                         |
|---------------|---------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere movido.                         |
| *Largura*       | Retorna a nova largura do quadro de caracteres (em pixels) como um inteiro.  |
| *Altura*      | Retorna a nova altura do quadro de caracteres (em pixels) como um inteiro. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento ocorre quando um aplicativo altera o tamanho de um caractere. Esse evento é enviado somente para os clientes do caractere (aplicativos que carregaram o caractere).

### <a name="see-also"></a>Consulte Também

[**Mover evento**](move-event.md)


 

 




