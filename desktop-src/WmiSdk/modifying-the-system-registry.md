---
description: O registro do sistema contém dados de configuração que o sistema operacional, os serviços e os aplicativos usam.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Modificando o registro do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33562e2747d63d8531ff2b23d07eadac33d830ef3ecf3b8613f22170c0b735ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992836"
---
# <a name="modifying-the-system-registry"></a>Modificando o registro do sistema

O registro do sistema contém dados de configuração que o sistema operacional, os serviços e os aplicativos usam. Windows A instrumentação de gerenciamento (WMI) tem um [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e a classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) com métodos que usam o para monitorar ou modificar o registro no computador local ou em computadores remotos. O [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider) dá suporte à classe de [**\_ registro do Win32**](/windows/desktop/CIMWin32Prov/win32-registry) que contém dados estáticos sobre o tamanho de um registro.

O provedor de registro do sistema é uma instância, uma propriedade e um provedor de eventos que se interfaces com o registro do sistema. O provedor de registro do sistema é um provedor padrão com a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Você pode usar o provedor de registro do sistema para acessar as informações e as chaves do registro em sistemas locais e remotos. Para obter mais informações, consulte [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider).

O WMI coloca o [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) no \\ namespace raiz padrão. No entanto, você pode compilar o arquivo Regevent. MOF em outros namespaces para que outros aplicativos usem.

Os tópicos identificados na tabela a seguir podem mostrar como usar a classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e o provedor de registro do sistema.



| Tópico                                                                                              | Descrição                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtendo dados do registro](obtaining-registry-data.md)                                             | Você pode obter ou modificar dados do registro por meio de métodos da classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) , que permite automatizar as atividades do registro localmente ou remotamente.                    |
| [Alterar dados de Registro](changing-registry-data.md)                                               | Você pode adicionar ou excluir chaves e adicionar ou alterar valores de entrada de registro em chaves.                                                                                                                    |
| [Programando com o provedor de registro do sistema](programming-with-the-system-registry-provider.md) | Você pode definir suas próprias classes que o registro do sistema fornece com dados.                                                                                                                       |
| [Registrando para eventos de registro do sistema](registering-for-system-registry-events.md)               | O provedor de registro do sistema pode enviar eventos para um consumidor. Para receber eventos, você deve registrar seu consumidor, criar uma consulta e, em seguida, garantir que o provedor esteja enviando eventos a você, corretamente. |
| [Registrando o provedor de registro do sistema](registering-the-system-registry-provider.md)           | O provedor de registro do sistema é registrado como parte do processo de instalação do WMI.                                                                                                                |



 

 

 
