---
title: Operações de conexão de discagem automática
description: Quando uma tentativa de conexão com um endereço de rede falha porque o host não pode ser acessado, o sistema pesquisa o banco de dados de mapeamento de discagem automática para o endereço.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150fa8542d1724be9d60f997db7952d6df387b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366108"
---
# <a name="autodial-connection-operations"></a>Operações de conexão de discagem automática

Quando uma tentativa de conexão com um endereço de rede falha porque o host não pode ser acessado, o sistema pesquisa o banco de dados de mapeamento de discagem automática para o endereço. Se o endereço estiver no banco de dados, o sistema iniciará uma operação de discagem automática para o [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), se houver, que corresponde ao local de discagem de TAPI local.

A API RAS fornece funções que permitem definir e consultar parâmetros de discagem automática que controlam conexões de discagem automática. Você pode chamar a função [**RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) para habilitar ou desabilitar o recurso de discagem automática para um local de discagem TAPI especificado. A função [**RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indica se o recurso de discagem automática está habilitado para um local de discagem TAPI especificado. Para obter mais informações sobre locais de discagem TAPI, consulte a documentação da TAPI. Você pode chamar a função [**RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) para definir outros parâmetros de conexão de discagem automática. Por exemplo, você pode desabilitar as conexões de discagem automática para a sessão de logon atual. Chame a função [**RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) para determinar o valor atual dos parâmetros de conexão de AutoDiscagem.

O sistema fornece uma interface de usuário padrão para operações de discagem automática. No entanto, você pode criar uma DLL (biblioteca de vínculo dinâmico) de discagem automática para fornecer uma interface de usuário personalizada para operações de discagem automática que envolvam entradas de catálogo telefônico especificadas. Sua DLL de AutoDiscagem deve exportar uma versão ANSI e uma Unicode de um manipulador de AutoDiscagem do [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) .

Para habilitar o manipulador de discagem automática personalizado para uma entrada de catálogo telefônico, chame a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir as propriedades dessa entrada. Os membros **szAutodialDll** e **SzAutodialFunc** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) passados para **RASSETENTRYPROPERTIES** especificam o nome da sua DLL de AutoDiscagem e o nome da função [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) , excluindo o sufixo "A" ou "W".

Quando o sistema inicia uma operação de discagem automática para uma entrada de catálogo telefônico com um manipulador de discagem automática personalizado, ele chama o [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)especificado. A função **RASADFunc** recebe um ponteiro para uma estrutura [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) que indica o local e a janela pai da janela da interface do usuário. Seu **RASADFunc** pode iniciar um thread para executar a operação de discagem personalizada. A função **RASADFunc** retorna **true** para indicar que levou sobre a discagem ou **false** para permitir que o sistema execute a discagem. Sua operação de discagem personalizada deve usar a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para fazer a discagem real. Quando a operação de discagem for concluída, a operação de discagem personalizada indica êxito ou falha ao definir a variável apontada pelo parâmetro *lpdwRetCode* passado para [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca).

 

 