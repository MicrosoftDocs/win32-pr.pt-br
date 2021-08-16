---
title: Remover método
description: Remover método
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3337fb25db49f1d6c8ccd6d94f2817340db226e14718cfa7943940fbfb069b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882777"
---
# <a name="remove-method"></a>Remover método

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Remove um objeto de [**comando**](/windows/desktop/lwef/the-command-object) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_"). Comandos. Remove_ o * _nome_



| Parte   | Descrição                                                       |
|--------|-------------------------------------------------------------------|
| *Nome* | Obrigatórios. Um valor de cadeia de caracteres correspondente à ID do comando. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando um objeto de [**comando**](/windows/desktop/lwef/the-command-object) é removido da coleção, ele não é mais exibido quando o menu pop-up do caractere é exibido ou na janela comandos quando seu aplicativo cliente está em entrada-ativo.

## <a name="see-also"></a>Consulte Também

[**Método RemoveAll**](removeall-method.md)


 

 