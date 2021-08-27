---
description: Explica como criar um pacote de segurança personalizado.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Criando pacotes de segurança personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88093ba7faed1ac2287c2a54391015984e83d4ad3878a60453978a9924706f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008844"
---
# <a name="creating-custom-security-packages"></a>Criando pacotes de segurança personalizados

## <a name="ssp-security-packages"></a>Pacotes de segurança do SSP

Se um pacote de segurança do SSP (provedor de suporte de segurança) personalizado for usado exclusivamente para o suporte de segurança de cliente/servidor, ele poderá implementar a [interface do provedor de suporte de segurança](sspi.md)da Microsoft.

O exemplo de SampSSP fornecido com o SDK (Software Development Kit) da plataforma contém uma implementação de pacote de segurança do SSP de exemplo.

## <a name="sspap-security-packages"></a>Pacotes de segurança do SSP/AP

Os [](/windows/desktop/SecGloss/s-gly) / [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly) do provedor de suporte de segurança personalizado (SSP/APS) contêm pacotes de segurança que funcionam como pacotes de autenticação (APS) e provedores de suporte de segurança (SSPs). Esses pacotes implementam APIs separadas para dar suporte a cada função.

Como ele funciona como um AP, um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) SSP/PA personalizado deve fornecer implementações para todas as [funções implementadas por pacotes de autenticação](authentication-functions.md).

Para fornecer suporte de segurança integrado, um pacote de segurança SSP/PA personalizado deve fornecer implementações para as [funções implementadas por SSP/APS](authentication-functions.md). As [funções LSA chamadas por SSP/APS](authentication-functions.md) descrevem as funções de suporte disponíveis para os desenvolvedores de SSP/PA que desejam interagir com a LSA.

Os pacotes de segurança do SSP/AP, para executar como um AP e um SSP, podem ser executados como parte do sistema operacional e como parte de um aplicativo de usuário. Esses dois modos de execução são conhecidos como modo LSA e modo de usuário, respectivamente. Para obter detalhes sobre os pacotes de segurança personalizados no modo LSA, consulte [inicialização do modo LSA](lsa-mode-initialization.md). Para obter detalhes sobre o modo de usuário, consulte [inicialização de modo de usuário](user-mode-initialization.md).

Se um pacote de segurança do SSP/AP personalizado oferecer serviços para aplicativos cliente/servidor, ele deverá fornecer implementações para as funções descritas em [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md). As [funções LSA chamadas pelo SSP/APS do modo de usuário](authentication-functions.md) descrevem as funções de suporte disponíveis para um SSP/AP em execução em um processo de cliente ou servidor.

Para obter informações sobre como registrar uma DLL SSP/PA, consulte [registrando DLLs SSP/PA](registering-ssp-ap-dlls.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições sobre o registro e a instalação de um pacote de segurança](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
