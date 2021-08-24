---
title: Restauração de BITS e do sistema
description: Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702096"
---
# <a name="bits-and-system-restore"></a>Restauração de BITS e do sistema

Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos. Se você retornar o computador a um ponto de restauração antes de uma atualização do BITS, a versão antiga do BITS poderá não ser capaz de ler as informações do trabalho atual. Se isso acontecer, o BITS excluirá a lista de trabalhos e criará uma nova lista de trabalhos vazia. Como resultado, os arquivos temporários associados à lista de trabalhos anteriores não são limpos; para recuperar o espaço em disco, você deve excluir os arquivos manualmente.

os usuários familiarizados com a linha de comando Windows podem evitar esse problema usando a [ferramenta BITSAdmin](bitsadmin-tool.md) para limpar a lista de trabalhos do BITS antes de executar a restauração do sistema. Para limpar a lista de trabalhos BITS, execute o seguinte comando:

**Bitsadmin/Reset reiniciar/AllUsers**

Observe que você deve ter privilégios de administrador para executar este comando.

 

 




