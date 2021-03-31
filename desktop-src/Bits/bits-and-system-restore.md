---
title: Restauração de BITS e do sistema
description: Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005058"
---
# <a name="bits-and-system-restore"></a>Restauração de BITS e do sistema

Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos. Se você retornar o computador a um ponto de restauração antes de uma atualização do BITS, a versão antiga do BITS poderá não ser capaz de ler as informações do trabalho atual. Se isso acontecer, o BITS excluirá a lista de trabalhos e criará uma nova lista de trabalhos vazia. Como resultado, os arquivos temporários associados à lista de trabalhos anteriores não são limpos; para recuperar o espaço em disco, você deve excluir os arquivos manualmente.

Os usuários familiarizados com a linha de comando do Windows podem evitar esse problema usando a [ferramenta BITSAdmin](bitsadmin-tool.md) para limpar a lista de trabalhos do bits antes de executar a restauração do sistema. Para limpar a lista de trabalhos BITS, execute o seguinte comando:

**Bitsadmin/Reset reiniciar/AllUsers**

Observe que você deve ter privilégios de administrador para executar este comando.

 

 




