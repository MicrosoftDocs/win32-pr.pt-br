---
description: O WMI é executado como parte de um host de serviço compartilhado com portas atribuídas por meio de DCOM por padrão. No entanto, você pode configurar o serviço WMI para ser executado como o único processo em um host separado e especificar uma porta fixa.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configurando uma porta fixa para o WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050244"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configurando uma porta fixa para o WMI

O WMI é executado como parte de um host de serviço compartilhado com portas atribuídas por meio de DCOM por padrão. No entanto, você pode configurar o serviço WMI para ser executado como o único processo em um host separado e especificar uma porta fixa.

O procedimento a seguir é uma configuração automatizada para permitir que o WMI tenha uma porta fixa. O procedimento usa a ferramenta de linha de comando [**winmgmt**](winmgmt.md) .

**Para configurar uma porta fixa para o WMI**

1.  No prompt de comando, digite **winmgmt-standalonehost**
2.  pare o serviço WMI digitando o comando **net stop "Instrumentação de Gerenciamento do Windows"** ou use o nome curto de **winmgmt do net stop**
3.  reinicie o serviço WMI novamente em um novo host de serviço digitando **net start "Instrumentação de Gerenciamento do Windows"** ou **net start winmgmt**
4.  Estabeleça um novo número de porta para o serviço WMI digitando **netsh firewall add abertura TCP 24158 WMIFixedPort**

Para desfazer as alterações feitas no WMI, digite **winmgmt/sharedhost** e, em seguida, pare e inicie o serviço Winmgmt novamente.

## <a name="examples"></a>Exemplos

Para obter um script que configura uma porta fixa para o WMI, consulte o [exemplo de código](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )da Galeria de scripts a seguir.

ou um exemplo de código do PowerShell que habilita ou desabilita as configurações de porta WMI, consulte o exemplo [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) na galeria do TechNet.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Solucionando problemas de conexões WMI remotas](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hospedagem e segurança de provedor](provider-hosting-and-security.md)
</dt> </dl>

 

 



