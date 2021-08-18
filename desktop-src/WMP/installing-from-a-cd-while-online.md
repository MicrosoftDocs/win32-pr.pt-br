---
title: Instalação de um CD enquanto estiver online
description: Instalação de um CD enquanto estiver online
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player online, instalando do CD enquanto online
- lojas online, instalando do CD enquanto online
- type 1 online stores,installing from CD while online
- type 2 online stores,installing from CD while online
- Windows Media Player online online, instalação online do CD
- online stores,online installs from CD
- type 1 online stores,online installs from CD
- type 2 online stores,online installs from CD
- Windows Media Player online, o CD é instalado enquanto online
- online stores,CD installs while online
- type 1 online stores,CD installs while online
- type 2 online stores,CD installs while online
- instalando lojas online do CD enquanto estiver online
- Instalação de CD de lojas online enquanto online
- instalação online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13589d7ba6dea0693acaacb5e0d1f551b4a4f178c4ccb50a1bd8ebb513dda3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996506"
---
# <a name="installing-from-a-cd-while-online"></a>Instalação de um CD enquanto estiver online

Os usuários podem instalar Windows Media Player de um CD enquanto estão conectados à Internet. Quando isso acontece, Windows Media Player configuração localiza o documento ServiceInfo especificado pelo parâmetro de linha de comando *ServiceInfo.* Se o **atributo Key** corresponde ao parâmetro de linha de comando *DefaultService,* a instalação inspecionará o elemento Install para personalizar o processo de instalação. Usando os valores de atributo, a instalação exibe seu EULA (Contrato de Licença de Usuário Final) e sua política de privacidade e também recupera e instala o arquivo .cab no computador do usuário. Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.

Depois que ele for instalado, Windows Media Player o armazenamento online inicial usando o nome da chave especificado para o parâmetro de linha de comando *DefaultService.*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Definindo a loja online inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configurar parâmetros de linha de comando para lojas online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




