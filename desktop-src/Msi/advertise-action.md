---
description: A ação de anúncio é uma ação de nível superior chamada para instalar ou remover componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Ação de anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662070"
---
# <a name="advertise-action"></a>Ação de anúncio

A ação de anúncio é uma ação de nível superior chamada para instalar ou remover componentes anunciados.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

O [*anúncio*](a-gly.md) refere-se à capacidade do instalador de fornecer as interfaces de carregamento e inicialização de um aplicativo sem instalar fisicamente o aplicativo. O instalador não instala os componentes necessários até que um usuário ou aplicativo ative uma interface anunciada. Esse conceito é chamado de [*instalação sob demanda*](i-gly.md).

A ação de anúncio não é chamada de dentro da sequência da tabela de ações, a Windows Installer executa essa ação quando o executável da linha de comando Msiexec.exe é chamado com a opção de linha de comando "/j" ou quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado com o parâmetro *SZCOMMANDLINE* definido como Action = Advertise.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



