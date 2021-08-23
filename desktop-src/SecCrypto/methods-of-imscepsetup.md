---
description: Métodos definidos pela interface IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Métodos de IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7dcadeb6c3815a37f1b1e87453a7ff737c70f53d76e0904bc67211ed7028f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622226"
---
# <a name="methods-of-imscepsetup"></a>Métodos de IMSCEPSetup

Os métodos a seguir são definidos pela interface [**IMSCEPSetup.**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de **IMSCEPSetup,** consulte [Propriedades de IMSCEPSetup](properties-of-imscepsetup.md).



| Método                                                             | Descrição                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Obtém a lista [*de comprimentos de chave*](../secgloss/k-gly.md) com suporte pelo CSP (provedor de serviços [*criptográficos)*](../secgloss/c-gly.md) especificado. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Obtém um valor da propriedade para uma configuração Serviço de Registro de Dispositivo de Rede (NDES).                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Obtém a lista de CSPs que fornecem assinatura de chave assimétrica e algoritmos de troca no computador.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inicializa um objeto **CMSCEPSetup** com valores padrão para habilitar a instalação de uma função NDES.                                                                                                                                                                                  |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Instala uma função conforme configurado no **objeto CMSCEPSetup.**                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Sempre retorna **VARIANT \_ TRUE** e não deve ser usado.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Este método não está implementado. Reservada para uso futuro.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Remove as configurações do Registro e do IIS para a função NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Define as informações da conta de usuário usadas pela extensão NDES do IIS para executar o registro em nome dos dispositivos de rede.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Define um valor da propriedade para uma configuração do NDES.                                                                                                                                                                                                                                  |



 

 

 
