---
description: A ação RegisterProduct registra as informações do produto com o instalador e com adicionar/remover programas. Além disso, essa ação armazena o pacote de banco de dados Windows Installer no computador local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Ação RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770178"
---
# <a name="registerproduct-action"></a>Ação RegisterProduct

A ação RegisterProduct registra as informações do produto com o instalador e com adicionar/remover programas. Além disso, essa ação armazena o pacote de banco de dados Windows Installer no computador local.

A ação RegisterProduct configura os controles exibidos por adicionar/remover programas no painel de controle. Para obter mais informações, consulte [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação            |
|-------|---------------------------------------|
| \[1\] | Informações sobre o produto registrado. |



 

## <a name="remarks"></a>Comentários

A ação RegisterProduct não é executada durante a instalação em um ponto de instalação administrativa.

 

 



