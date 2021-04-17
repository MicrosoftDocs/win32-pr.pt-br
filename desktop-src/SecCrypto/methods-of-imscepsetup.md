---
description: Métodos definidos pela interface IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Métodos de IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501882"
---
# <a name="methods-of-imscepsetup"></a>Métodos de IMSCEPSetup

Os métodos a seguir são definidos pela interface [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) . Os métodos de acesso à propriedade não são mostrados aqui. Para ver as propriedades de **IMSCEPSetup**, consulte [Propriedades de IMSCEPSetup](properties-of-imscepsetup.md).



| Método                                                             | Descrição                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Obtém a lista de [*comprimentos de chave*](../secgloss/k-gly.md) com suporte pelo CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) especificado. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Obtém um valor de propriedade para uma configuração de NDES (serviço de registro de dispositivo de rede).                                                                                                                                                                                               |
| [**Getprovidernamelist**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Obtém a lista de CSPs que fornecem a assinatura de chave assimétrica e algoritmos de troca no computador.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Inicializa um objeto **CMSCEPSetup** com valores padrão para habilitar a instalação de uma função de NDES.                                                                                                                                                                                  |
| [**Instalar**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Instala uma função como configurada no objeto **CMSCEPSetup** .                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Sempre retorna a **variante \_ true** e não deve ser usada.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Este método não está implementado. Reservada para uso futuro.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Remove as configurações do registro e do IIS para a função NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Define as informações de conta de usuário usadas pela extensão de NDES do IIS para executar o registro em nome dos dispositivos de rede.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Define um valor de propriedade para uma configuração de NDES.                                                                                                                                                                                                                                  |



 

 

 
