---
description: As caixas de diálogo são especificadas na coluna caixa de diálogo da tabela de diálogo. Para obter mais informações sobre como adicionar uma caixa de diálogo ou um mural a uma interface do usuário, consulte usando a interface do usuário.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Caixas de diálogo (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170239"
---
# <a name="dialog-boxes-windows-installer"></a>Caixas de diálogo (Windows Installer)

As caixas de diálogo são especificadas na coluna caixa de diálogo da [tabela de diálogo](dialog-table.md). Para obter mais informações sobre como adicionar uma caixa de diálogo ou um mural a uma interface do usuário, consulte [usando a interface do usuário](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nomes de caixas de diálogo reservadas

Os nomes da caixa de diálogo a seguir são reservados pelo Windows Installer e não devem ser usados para caixas de diálogo personalizadas criadas pelo usuário. O instalador requer que essas caixas de diálogo sejam listadas na [tabela de diálogo](dialog-table.md) usando os nomes reservados a seguir. Cada caixa de diálogo e nome só podem ser listados uma vez. Os desenvolvedores devem criar essas caixas de diálogo na interface do usuário. Para obter informações sobre como visualizar as caixas de diálogo, consulte [importando a interface do usuário](importing-the-user-interface.md).



| Nome da caixa de diálogo                                      | Breve descrição da caixa de diálogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caixa de diálogo FilesInUse](filesinuse-dialog.md)           | Alerta o usuário para processar a substituição ou exclusão de arquivos.                                                                                                                 |
| [Caixa de diálogo FirstRun](firstrun-dialog.md)               | Coleta o nome de usuário, o nome da empresa e a ID do produto.                                                                                                                       |
| [Caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Alerta o usuário para processar a substituição ou exclusão de arquivos e dá ao usuário a opção de usar o [Gerenciador de reinicialização](/windows/desktop/RstMgr/restart-manager-portal) para fechar e reiniciar aplicativos. |



 

## <a name="required-dialog-boxes"></a>Caixas de diálogo necessárias

Durante a instalação, determinados eventos fazem Windows Installer verificar as [tabelas de sequência da interface do usuário](using-a-sequence-table.md) no pacote e exibir a caixa de diálogo especificada. Por exemplo, no caso de um erro fatal, Windows Installer exibe a caixa de diálogo que é listada com um número de sequência de-3 na tabela de sequência da interface do usuário, independentemente da caixa de diálogo nomeada na [tabela de diálogo](dialog-table.md). A tabela a seguir lista os eventos específicos e seu número de sequência correspondente na tabela de sequências da interface do usuário:



| Tipo de evento                        | Número de sequência da tabela de sequência da interface do usuário | Descrição da caixa de diálogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Erro fatal](fatalerror-dialog.md) | -3                                            | A instalação foi encerrada por um erro fatal.      |
| [Saída do usuário](userexit-dialog.md)     | -2                                            | A instalação foi encerrada na solicitação do usuário. |
| [Sair](exit-dialog.md)              | -1                                            | A instalação foi concluída com êxito.               |



 

Além disso, o autor do pacote deve criar uma caixa de diálogo genérica para exibir Windows Installer mensagens de [erro](error-dialog.md) . Essa caixa de diálogo pode ser nomeada como qualquer coisa, mas esse nome deve ser especificado na propriedade **ErrorDialog** .

## <a name="typical-dialog-boxes"></a>Caixas de diálogo típicas

As caixas de diálogo a seguir são opcionais e normalmente são incluídas na interface do usuário criada de um pacote de instalação. Essas caixas de diálogo são típicas da maioria dos [assistentes de interface do usuário](user-interface-wizard-behavior.md) para instalação de arquivos. Essas caixas de diálogo podem ter qualquer nome na tabela de diálogo. Os nomes mostrados são recomendados apenas para fins de clareza e podem ser modificados conforme necessário. Por exemplo, duas caixas de diálogo **LicenseAgreement** personalizadas diferentes podem ser usadas no pacote e diferenciadas na tabela de diálogo pelos nomes ProfessionalLicenseAgreement e LimitedLicenseAgreement.



| Tipo de caixa de diálogo                                             | Breve descrição da caixa de diálogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Caixa de diálogo DiskCost](diskcost-dialog.md)                  | Indica espaço em disco insuficiente para a instalação. |
| [Caixa de diálogo Procurar](browse-dialog.md)                      | Permite que o usuário selecione um diretório.                     |
| [Caixa de diálogo cancelar](cancel-dialog.md)                      | Confirma uma solicitação para encerrar a instalação.       |
| [Caixa de diálogo contrato de licença](licenseagreement-dialog.md) | Caixa modal exibindo o contrato de licença.             |
| [Caixa de diálogo de seleção](selection-dialog.md)                | Caixa modal que permite ao usuário selecionar itens.            |



 

 

 
