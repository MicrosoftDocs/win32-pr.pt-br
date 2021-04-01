---
description: Instalações simultâneas, também chamadas de instalações aninhadas, são um recurso preterido do Windows Installer.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Instalações simultâneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829014"
---
# <a name="concurrent-installations"></a>Instalações simultâneas

Instalações simultâneas, também chamadas de instalações aninhadas, são um recurso preterido do Windows Installer. Os aplicativos instalados com instalações simultâneas podem eventualmente falhar porque são difíceis para os clientes atenderem corretamente. Não use instalações simultâneas para instalar produtos que devem ser liberados para o público. As instalações simultâneas podem ter aplicabilidade limitada em ambientes corporativos controlados quando usadas para instalar aplicativos que não são destinados à versão pública. A documentação de instalações simultâneas é fornecida para os autores de pacotes que desejam usar instalações simultâneas com aplicativos que não são para distribuição pública.

Uma ação de instalação simultânea instala outro pacote de Windows Installer durante uma instalação em execução no momento. Uma instalação simultânea é adicionada a um pacote por meio da criação de uma ação de instalação simultânea na [tabela CustomAction](customaction-table.md) e do agendamento dessa ação personalizada nas tabelas de sequência. O campo de destino da tabela CustomAction contém uma cadeia de caracteres das configurações de propriedade pública usadas pela instalação simultânea. O campo de origem da tabela CustomAction identifica o pacote simultâneo. Uma ação de instalação simultânea só pode reinstalar ou remover um aplicativo que foi instalado pelo pacote de instalação do aplicativo atual.

O tipo de ação de instalação simultânea é especificado no campo tipo da tabela CustomAction. Dependendo do tipo de ação personalizada, o pacote para o aplicativo simultâneo pode residir em um subarmazenamento do pacote principal, como um arquivo em um local especificado por uma propriedade ou como um aplicativo anunciado no computador do usuário. Os seguintes tipos de ações personalizadas executam uma instalação simultânea.



| Tipo de ação personalizada                                 | Descrição                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo de ação personalizada 7](custom-action-type-7.md)   | Instalação simultânea de um produto que reside no pacote de instalação.      |
| [Tipo de ação personalizada 23](custom-action-type-23.md) | Instalação simultânea de um pacote do instalador na árvore de origem atual. |
| [Tipo de ação personalizada 39](custom-action-type-39.md) | Instalação simultânea de um pacote do instalador anunciado.                     |



 

Uma instalação simultânea compartilha a mesma interface do usuário e configurações de log como a instalação principal.

As ações de instalação simultânea devem ser colocadas entre a [ação InstallInitialize](installinitialize-action.md) e a [ação InstallFinalize](installfinalize-action.md) da sequência de ação da instalação principal. Após a reversão da instalação principal, o instalador irá reverter a instalação simultânea também. O uso da [execução adiada](deferred-execution-custom-actions.md) com ações de instalação simultânea é desnecessário porque o instalador combina informações de reversão das instalações simultâneas e principais. Todas as alterações são revertidas após uma instalação de reversão.

Os valores de retorno para ações de instalação simultânea são os mesmos para outras ações personalizadas. Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).

As ações padrão ou personalizadas que especificam uma reinicialização automática do sistema ou solicitam que o usuário reiniciem também podem executar reinicialização ou solicitação de dentro de uma instalação simultânea.

Depois que o instalador inicia uma instalação simultânea, ele bloqueia todas as outras instalações até que a instalação simultânea seja concluída e antes de continuar a instalação principal. O instalador só pode executar instalações simultâneas como ações personalizadas síncronas. Consulte [ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md). Os sinalizadores de opção descritos em [Opções de processamento de retorno de ação personalizadas](custom-action-return-processing-options.md) devem ser definidos como nenhum (+ 0) ou **msidbCustomActionTypeContinue** (+ 64).

Uma ação de instalação simultânea pode instalar um aplicativo para ser executado localmente, para ser executado da origem, para ser reinstalado ou para ser removido da mesma maneira que ao usar o [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para uma instalação normal. Para especificar o tipo de instalação, passe a propriedade [**ADDLOCAL**](addlocal.md), [**addsource**](addsource.md), [**REINSTALL**](reinstall.md)ou [**Remove**](remove.md) para a ação de instalação simultânea.

As ações de instalação simultânea podem ser criadas em pares, uma ação usada para instalar e a outra ação usada para remover a instalação simultânea. Um [tipo de ação personalizada 7](custom-action-type-7.md) ou [tipo de ação personalizada 23](custom-action-type-23.md) normalmente é usado para instalar o. Um [tipo de ação personalizada 39](custom-action-type-39.md) normalmente é usado para remover a instalação simultânea quando o produto pai é desinstalado. O registro para a ação personalizada de remoção na [tabela CustomAction](customaction-table.md) pode ter o GUID de código do produto no campo de origem e "Remove = All" no campo de destino. As duas ações personalizadas precisam ser criadas na tabela de sequência de ação com condições mutuamente exclusivas. Por exemplo, a ação personalizada que instala o produto pode ter "não instalado" em seu campo de condição e a ação personalizada remove a instalação simultânea pode ter REMOVE = "ALL" em seu campo de condição.

Não há nenhum método para consultar um pacote por seu custo. Isso torna difícil o custo de instalações simultâneas. As linhas devem ser adicionadas à [tabela ReserveCost](reservecost-table.md) para indicar as pastas e os custos de pior caso do componente associado à instalação simultânea.

As únicas [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md) disponíveis com ações de instalação simultâneas são None (+ 0) ou **msidbCustomActionTypeContinue** (+ 64).

Observe que uma instalação pai não pode chamar seu próprio pacote como uma ação de instalação simultânea.

Observe que, se uma instalação por máquina tentar executar uma instalação simultânea por usuário, o instalador registrará a instalação pai como por usuário por padrão. Isso pode fazer com que o instalador remova incorretamente o aplicativo, pois o instalador tenta desinstalar o aplicativo por máquina quando ele está realmente registrado como por usuário. Para forçar o estado de uma instalação simultânea para acompanhar o estado de sua instalação pai, insira ALLUSERS = " \[ AllUsers \] " na coluna de destino da [tabela CustomAction](customaction-table.md). Nesse caso, a instalação simultânea será por máquina se o pai for por máquina, e a instalação simultânea será por usuário se o pai for por usuário.

Os desenvolvedores devem observar os seguintes avisos ao criar instalações simultâneas.

-   As instalações simultâneas não podem compartilhar componentes.
-   Uma instalação administrativa também não pode conter uma instalação simultânea.
-   A aplicação de patches e a atualização podem não funcionar com instalações simultâneas.
-   O instalador pode não custar corretamente uma instalação simultânea.
-   ProgressBars integradas não podem ser usadas com instalações simultâneas.
-   Os recursos que devem ser anunciados não podem ser instalados pela instalação simultânea.
-   Um pacote que executa uma instalação simultânea de um aplicativo também deve desinstalar o aplicativo simultâneo quando o produto pai é desinstalado.

Para impedir que um pacote nunca seja instalado como uma instalação simultânea, adicione uma das instruções condicionais a seguir à tabela [LaunchCondition](launchcondition-table.md) . Isso impede que o pacote nunca seja instalado por uma ação de instalação simultânea executada por outra instalação. Isso não impede que o pacote seja removido pela ação [RemoveExistingProducts](removeexistingproducts-action.md) . Consulte também a propriedade [**ParentOriginalDatabase**](parentoriginaldatabase.md) e a propriedade [**ParentProductCode**](parentproductcode.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



