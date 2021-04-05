---
description: Os métodos a seguir são definidos pela interface ICertSrvSetup. Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de ICertSrvSetup, consulte Propriedades de ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Métodos de ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e3482de2c8c62db854b86d21e739993bc3bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827249"
---
# <a name="methods-of-icertsrvsetup"></a>Métodos de ICertSrvSetup

Os métodos a seguir são definidos pela interface [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) . Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de **ICertSrvSetup**, consulte [Propriedades de ICertSrvSetup](properties-of-icertsrvsetup.md).



| Método                                                                         | Descrição                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importa um certificado de autoridade de certificação (CA) e sua chave privada associada para o repositório "LocalMachine".                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Obtém um valor de propriedade para uma configuração de autoridade de certificação.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Obtém a coleção de objetos **CCertSrvSetupKeyInformation** que representam certificados de autoridade de certificação válidos atualmente instalados no computador.                                                                                                                  |
| [**Gethashalgorithmlist**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Obtém a lista de algoritmos de hash com suporte pelo CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) especificado para um algoritmo de assinatura de chave assimétrica. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Obtém a lista de comprimentos de chave com suporte pelo CSP especificado.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Obtém a lista de nomes de contêiner de chave armazenados pelo CSP especificado para algoritmos de chave de assinatura assimétrica.                                                                                                                                                 |
| [**Getprovidernamelist**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Obtém a lista de CSPs que fornecem algoritmos de assinatura de chave assimétrica no computador.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Obtém os tipos de CAs que podem ser instalados em um computador sob o contexto do chamador.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Inicializa um objeto **CCertSrvSetup** com valores padrão para habilitar a instalação de uma função de autoridade de certificação.                                                                                                                                                           |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Instala uma função de autoridade de certificação conforme configurado no objeto **CCertSrvSetup** .                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indica ao chamador se uma propriedade especificada pode ser editada.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | Não está implementado e está reservado para uso futuro.                                                                                                                                                                                                        |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Salva temporariamente o estado específico da função-informações.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Define um nome comum de autoridade de certificação e um sufixo de nome distinto opcional.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Define um valor de propriedade para uma configuração de autoridade de certificação.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Define as informações relacionadas ao banco de dados para a função de autoridade de certificação.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Define as informações da autoridade de certificação pai para uma configuração de autoridade de certificação subordinada.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Define as informações de autoridade de certificação para a função de registro na Web da autoridade de certificação.                                                                                                                                                                                                   |



 

 

 
