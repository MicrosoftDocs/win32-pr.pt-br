---
title: Marca LST
description: Marca LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498697"
---
# <a name="lst-tag"></a>Marca LST

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Repete a última instrução falada para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

\\**Ficheiro**\\

</dd> </dl>

### <a name="remarks"></a>Comentários

Essa marca permite que um caractere repita sua última instrução falada. Essa marca deve aparecer por si só no método [**Speak**](speak-method.md) ; nenhum outro texto ou parâmetro pode ser incluído. Quando o texto falado é repetido, todas as outras marcas incluídas no texto original são repetidas, exceto os indicadores. Outro. WAV e. Os arquivos LWV incluídos no texto também são repetidos.

 

 




