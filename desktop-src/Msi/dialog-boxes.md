---
description: As caixas de diálogo são especificadas na coluna Diálogo da tabela Diálogo. Para obter mais informações sobre como adicionar uma caixa de diálogo ou uma caixa de diálogo a uma interface do usuário, consulte Usando o Interface do Usuário.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Caixas de diálogo (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38da0e4d562854abc32064eee06a303747c2587591a5526ae98177a13e0462a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764056"
---
# <a name="dialog-boxes-windows-installer"></a>Caixas de diálogo (Windows Instalador)

As caixas de diálogo são especificadas na coluna Diálogo da [tabela Dialog](dialog-table.md). Para obter mais informações sobre como adicionar uma caixa de diálogo ou uma caixa de diálogo a uma interface do usuário, consulte [Usando o Interface do Usuário](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nomes da caixa de diálogo reservada

Os nomes de caixa de diálogo a seguir são reservados pelo Windows Instalador e não devem ser usados para nenhuma caixa de diálogo personalizada de usuário. O instalador requer que essas caixas de diálogo sejam listadas na tabela [Diálogo usando](dialog-table.md) os seguintes nomes reservados. Cada caixa de diálogo e nome só podem ser listados uma vez. Os desenvolvedores devem fazer essas caixas de diálogo na interface do usuário. Para obter informações sobre como visualizar caixas de diálogo, [consulte Importando o Interface do Usuário](importing-the-user-interface.md).



| Nome da caixa de diálogo                                      | Breve descrição da caixa de diálogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caixa de diálogo FilesInUse](filesinuse-dialog.md)           | Alerta o usuário para processos de substituição ou exclusão de arquivos.                                                                                                                 |
| [Caixa de diálogo FirstRun](firstrun-dialog.md)               | Coleta o nome de usuário, o nome da empresa e a ID do produto.                                                                                                                       |
| [Caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Alerta o usuário para processos de substituição ou exclusão de arquivos e fornece ao usuário a opção de usar o [Gerenciador](/windows/desktop/RstMgr/restart-manager-portal) de Reinicialização para fechar e reiniciar aplicativos. |



 

## <a name="required-dialog-boxes"></a>Caixas de diálogo necessárias

Durante a instalação, determinados eventos Windows instalador verificam as tabelas de sequência de [interface](using-a-sequence-table.md) do usuário no pacote e exibem a caixa de diálogo especificada. Por exemplo, no caso de um erro fatal, o instalador do Windows exibe a caixa de diálogo listada com um número de sequência de -3 na tabela de sequência da interface do usuário, independentemente de qual caixa de diálogo é nomeada na tabela Diálogo [.](dialog-table.md) A tabela a seguir lista os eventos específicos e seu número de sequência correspondente na tabela de sequência de interface do usuário:



| Tipo de evento                        | Número de sequência de tabela de sequência de interface do usuário | Descrição da caixa de diálogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Erro fatal](fatalerror-dialog.md) | -3                                            | A instalação foi encerrada por um erro fatal.      |
| [Saída do usuário](userexit-dialog.md)     | -2                                            | A instalação foi encerrada por solicitação do usuário. |
| [Sair](exit-dialog.md)              | -1                                            | A instalação foi concluída com êxito.               |



 

Além disso, o autor do pacote deve criar uma caixa de diálogo genérica para exibir Windows de erro [do](error-dialog.md) Instalador. Essa caixa de diálogo pode ser nomeada qualquer coisa, mas esse nome deve ser especificado na **propriedade ErrorDialog.**

## <a name="typical-dialog-boxes"></a>Caixas de diálogo típicas

As caixas de diálogo a seguir são opcionais e normalmente estão incluídas na interface do usuário autor de um pacote de instalação. Essas caixas de diálogo são típicas da maioria [dos assistentes de interface do usuário](user-interface-wizard-behavior.md) para instalar arquivos. Essas caixas de diálogo podem ter qualquer nome na tabela Diálogo. Os nomes mostrados são recomendados apenas para maior clareza e podem ser modificados conforme necessário. Por exemplo, duas caixas de diálogo **LicenseAgreement** personalizadas diferentes podem ser usadas no pacote e diferenciadas na tabela Diálogo pelos nomes ProfessionalLicenseAgreement e LimitedLicenseAgreement.



| Tipo de caixa de diálogo                                             | Breve descrição da caixa de diálogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Caixa de diálogo DiskCost](diskcost-dialog.md)                  | Indica espaço em disco insuficiente para a instalação. |
| [Caixa de diálogo Procurar](browse-dialog.md)                      | Permite que o usuário selecione um diretório.                     |
| [Caixa de diálogo Cancelar](cancel-dialog.md)                      | Confirma uma solicitação para encerrar a instalação.       |
| [Caixa de diálogo Contrato de Licença](licenseagreement-dialog.md) | Caixa modal exibindo o contrato de licença.             |
| [Caixa de diálogo Seleção](selection-dialog.md)                | Caixa modal permitindo que o usuário selecione itens.            |



 

 

 
