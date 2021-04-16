---
description: Quando uma operação de backup do VSS é realizada sem o envolvimento de um gravador, a criação da cópia de sombra ainda pode ocorrer.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Backups sem participação no gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750187"
---
# <a name="backups-without-writer-participation"></a>Backups sem participação no gravador

Quando uma operação de backup do VSS é realizada sem o envolvimento de um gravador, a criação da cópia de sombra ainda pode ocorrer.

Conforme observado em outro lugar (consulte o [estado de cópia de sombra padrão](shadow-copies-and-shadow-copy-sets.md)), o resultado desse tipo de cópia de sombra é um volume que reflete o estado de um disco no momento da cópia de sombra: os dados no volume copiado por sombra podem refletir operações de e/s incompletas ou parciais e são descritos como estando em um [*estado consistente de falha*](vssgloss-c.md).

Há várias situações que exigirão que um aplicativo de backup funcione com dados copiados de sombra consistente com falhas:

-   **Os dados são gerenciados por aplicativos sem reconhecimento de VSS**

    Quase todos os sistemas terão alguns aplicativos: editores de texto, leitores de email, processadores de texto e assim por diante – que não sabem VSS, portanto, é sempre provável que alguns dos dados em uma cópia de sombra precisem ser considerados como estando em um estado consistente de falha.

    Esse tipo de dados normalmente não é crítico ao sistema ou ao serviço, portanto, o backup dele não deve ser problemático ou, pelo menos, não mais problemático do que durante um backup convencional.

    Assim como acontece com os backups convencionais, se possível, os operadores de backup devem tentar suspender ou encerrar esses aplicativos antes de iniciar um trabalho de backup do VSS.

-   **Sistema sem gravadores compatíveis com VSS**

    Essa situação pode ser relativamente rara, pois a maioria dos sistemas cujo backup pode ser feito por um aplicativo de backup do VSS terá uma versão do Windows habilitada para o VSS, que deve conter gravadores.

    No entanto, há determinadas circunstâncias em que esse problema pode surgir — por exemplo, se você estiver fazendo backup de um sistema sem suporte a VSS, mas o sistema usar um dispositivo em rede habilitado para VSS para seu armazenamento.

    Embora o backup do estado do sistema de uma imagem consistente com falhas não seja o ideal, pode ser suficiente para um computador reiniciar a um status operacional. Em muitos casos, o computador será recuperado de todas as operações de e/s incompletas para os sistemas de arquivos e funcionará normalmente.

-   **Um solicitante optando por não trabalhar com os gravadores de sistema**

    Essa circunstância ocorreria se um solicitante optasse por não adicionar nenhum componente de gravador ou desabilitar todos os gravadores.

    A realização de backups dessa maneira geralmente não é recomendável. Embora o volume de sombra copiado para backup possa ser suficiente para restaurar um sistema para em execução, ele não é desejável. Na verdade, como os gravadores em execução no sistema são projetados com a funcionalidade para cooperar com as cópias de sombra e VSS, o backup de seus dados dessa maneira pode resultar em instabilidade.

 

 



