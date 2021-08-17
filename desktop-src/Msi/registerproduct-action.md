---
description: A ação RegisterProduct registra as informações do produto com o instalador e com Adicionar/Remover Programas. Além disso, essa ação armazena o pacote Windows banco de dados do instalador no computador local.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: Ação RegisterProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375956"
---
# <a name="registerproduct-action"></a>Ação RegisterProduct

A ação RegisterProduct registra as informações do produto com o instalador e com Adicionar/Remover Programas. Além disso, essa ação armazena o pacote Windows banco de dados do instalador no computador local.

A ação RegisterProduct configura os controles exibidos pela ação Adicionar/Remover Programas Painel de Controle. Para obter mais informações, [consulte Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação            |
|-------|---------------------------------------|
| \[1\] | Informações sobre o produto registrado. |



 

## <a name="remarks"></a>Comentários

A ação RegisterProduct não é executada durante a instalação em um ponto de instalação administrativa.

 

 



