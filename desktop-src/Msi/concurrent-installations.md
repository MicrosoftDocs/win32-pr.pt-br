---
description: Instalações simultâneas, também chamadas de Instalações Aninhadas, é um recurso preterido do Windows Instalador.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Instalações simultâneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09264df8c47c08f7d1512b46d65572d3572d5190f960254c8ed13182dd668657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144403"
---
# <a name="concurrent-installations"></a>Instalações simultâneas

Instalações simultâneas, também chamadas de Instalações Aninhadas, é um recurso preterido do Windows Instalador. Os aplicativos instalados com instalações simultâneas podem eventualmente falhar porque são difíceis para os clientes atenderem corretamente. Não use instalações simultâneas para instalar produtos destinados a serem liberados para o público. Instalações simultâneas podem ter aplicabilidade limitada em ambientes corporativos controlados quando usadas para instalar aplicativos que não se destinam à versão pública. A documentação de instalações simultâneas é fornecida para autores de pacote que desejam usar instalações simultâneas com aplicativos que não são para distribuição pública.

Uma ação de instalação simultânea instala outro Windows instalador durante uma instalação em execução no momento. Uma instalação simultânea é adicionada a um pacote por meio da adoção de uma ação de instalação simultânea na tabela [CustomAction](customaction-table.md) e do agendamento dessa ação personalizada nas tabelas de sequência. O campo Destino da tabela CustomAction contém uma cadeia de caracteres de configurações de propriedade pública usadas pela instalação simultânea. O campo Origem da tabela CustomAction identifica o pacote simultâneo. Uma ação de instalação simultânea só pode reinstalar ou remover um aplicativo que foi instalado pelo pacote de instalação do aplicativo atual.

O tipo de ação de instalação simultânea é especificado no campo Tipo da tabela CustomAction. Dependendo do tipo de ação personalizada, o pacote para o aplicativo simultâneo pode residir em um substorage do pacote principal, como um arquivo em um local especificado por uma propriedade ou como um aplicativo anunciado no computador do usuário. Os seguintes tipos de ações personalizadas executam uma instalação simultânea.



| Tipo de ação personalizado                                 | Descrição                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Tipo de ação personalizada 7](custom-action-type-7.md)   | Instalação simultânea de um produto que reside no pacote de instalação.      |
| [Tipo de ação personalizada 23](custom-action-type-23.md) | Instalação simultânea de um pacote do instalador na árvore de origem atual. |
| [Tipo de ação personalizada 39](custom-action-type-39.md) | Instalação simultânea de um pacote do instalador anunciado.                     |



 

Uma instalação simultânea compartilha a mesma interface do usuário e configurações de log que a instalação principal.

As ações de instalação simultâneas devem ser colocadas entre a ação [InstallInitialize](installinitialize-action.md) e a ação [InstallFinalize](installfinalize-action.md) da sequência de ação da instalação principal. Após a reação da instalação principal, o instalador também reverterá a instalação simultânea. O uso da [execução adiada](deferred-execution-custom-actions.md) com ações de instalação simultâneas é desnecessário porque o instalador combina informações de retorção das instalações simultâneas e principais. Todas as alterações são revertidas após uma instalação de reversão.

Os valores de retorno para ações de instalação simultâneas são os mesmos que para outras ações personalizadas. Consulte [Valores de retorno de ação personalizada.](custom-action-return-values.md)

Ações padrão ou personalizadas que especificam uma reinicialização automática do sistema ou solicitam que o usuário reinicie também podem executar reinicialização ou solicitação de dentro de uma instalação simultânea.

Depois que o instalador inicia uma instalação simultânea, ele bloqueia todas as outras instalações até que a instalação simultânea seja concluída e antes de continuar a instalação principal. O instalador só pode executar instalações simultâneas como ações personalizadas síncronas. Consulte [Ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md). Os sinalizadores de [](custom-action-return-processing-options.md) opção descritos em Opções de Processamento de Retorno de Ação Personalizada devem ser definidos como nenhum (+0) ou **msidbCustomActionTypeContinue** (+64).

Uma ação de instalação simultânea pode instalar um aplicativo a ser executado localmente, executar da origem, ser reinstalado ou ser removido da mesma maneira que ao usar [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) para uma instalação regular. Para especificar o tipo de instalação, passe a propriedade [**ADDLOCAL**](addlocal.md), [**ADDSOURCE**](addsource.md), [**REINSTALL**](reinstall.md)ou [**REMOVE**](remove.md) para a ação de instalação simultânea.

As ações de instalação simultâneas podem ser desenvolvidas em pares, uma ação usada para instalar e a outra ação usada para remover a instalação simultânea. Um [Tipo de Ação Personalizada 7](custom-action-type-7.md) ou Tipo de Ação Personalizada [23](custom-action-type-23.md) normalmente é usado para instalar. Um [Tipo de Ação Personalizada 39](custom-action-type-39.md) normalmente é usado para remover a instalação simultânea quando o produto pai é desinstalado. O registro para a ação personalizada de remoção na tabela [CustomAction](customaction-table.md) pode ter o GUID do código do produto no campo Origem e "REMOVE=ALL" no campo Destino. As duas ações personalizadas precisam ser feitas na tabela de sequência de ação com condições mutuamente exclusivas. Por exemplo, a ação personalizada que instala o produto pode ter "NOT Installed" em seu campo Condição e a ação personalizada remove a instalação simultânea pode ter REMOVE="ALL" em seu campo Condição.

Não há nenhum método para consultar um pacote para seu custo. Isso dificulta o custo de instalações simultâneas. As linhas devem ser adicionadas à tabela [ReserveCost](reservecost-table.md) para indicar as pastas e os custos de pior caso do componente associado à instalação simultânea.

As únicas [opções de](custom-action-return-processing-options.md) processamento de retorno de ação personalizada disponíveis com ações de instalação simultâneas são nenhuma (+0) ou **msidbCustomActionTypeContinue** (+64).

Observe que uma instalação pai não pode chamar seu próprio pacote como uma ação de instalação simultânea.

Observe que, se uma instalação por computador tentar executar uma instalação simultânea por usuário, o instalador registrará a instalação pai como por usuário por padrão. Isso pode fazer com que o instalador remova incorretamente o aplicativo porque o instalador tenta desinstalar o aplicativo por computador quando ele está realmente registrado como por usuário. Para forçar o estado de uma instalação simultânea a acompanhar o estado de sua instalação pai, insira ALLUSERS=" ALLUSERS " na coluna Destino da tabela \[ \] [CustomAction](customaction-table.md). Nesse caso, a instalação simultânea será por computador se o pai for por computador e a instalação simultânea for por usuário se o pai for por usuário.

Os desenvolvedores devem observar os avisos a seguir ao autorizar instalações simultâneas.

-   Instalações simultâneas não podem compartilhar componentes.
-   Uma instalação administrativa também não pode conter uma instalação simultânea.
-   A a patch e a atualização podem não funcionar com instalações simultâneas.
-   O instalador pode não custar corretamente uma instalação simultânea.
-   ProgressBars integrados não podem ser usados com instalações simultâneas.
-   Os recursos que devem ser anunciados não podem ser instalados pela instalação simultânea.
-   Um pacote que executa uma instalação simultânea de um aplicativo também deve desinstalar o aplicativo simultâneo quando o produto pai é desinstalado.

Para impedir que um pacote seja instalado como uma instalação simultânea, adicione uma das seguintes instruções condicionais à [tabela LaunchCondition.](launchcondition-table.md) Isso impede que o pacote seja instalado por uma ação de instalação simultânea executado por outra instalação. Isso não impede que o pacote seja removido pela [ação RemoveExistingProducts.](removeexistingproducts-action.md) Consulte também a [**propriedade ParentOriginalDatabase**](parentoriginaldatabase.md) e [**a propriedade ParentProductCode.**](parentproductcode.md)

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



