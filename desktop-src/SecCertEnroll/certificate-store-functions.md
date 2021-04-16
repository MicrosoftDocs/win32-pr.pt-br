---
description: 'A biblioteca de Xenroll.dll contém os seguintes métodos e propriedades que você pode usar para gerenciar repositórios de certificados. FunctionsDescriptionCAStoreFlagsSpecifies ou retorna sinalizadores que controlam o acesso ao armazenamento da autoridade de certificação (CA). CAStoreNameWStrSpecifies ou retorna o nome do repositório de autoridade de certificação. CAStoreTypeWStrSpecifies ou retorna o tipo do repositório identificado pela propriedade CAStoreName. MyStoreFlagsSpecifies ou retorna um sinalizador que determina o caminho do repositório pessoal. MyStoreNameWStrSpecifies ou retorna o nome do repositório pessoal. MyStoreTypeWStrSpecifies ou retorna o tipo do repositório pessoal. RequestStoreFlagsSpecifies ou retorna um sinalizador que determina o caminho do repositório de solicitações. RequestStoreNameWStrSpecifies ou retorna o nome do repositório de solicitações. RequestStoreTypeWStrSpecifies ou retorna o tipo do repositório de solicitações. RootStoreFlagsSpecifies ou retorna um sinalizador que determina o caminho do repositório raiz. RootStoreNameWStrSpecifies ou retorna o nome do repositório raiz. RootStoreTypeWStrSpecifies ou retorna o tipo do repositório raiz. SetHStoreCASpecifies o identificador do repositório de CA. SetHStoreMySpecifies o identificador do armazenamento pessoal. SetHStoreRequestSpecifies o identificador do repositório de solicitações. SetHStoreROOTSpecifies o identificador do repositório raiz. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Funções de repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00ab4b7245f999e1131f41172b3c77af8b9c2aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758171"
---
# <a name="certificate-store-functions"></a>Funções de repositório de certificados

A biblioteca de Xenroll.dll contém os seguintes métodos e propriedades que você pode usar para gerenciar repositórios de certificados.

| Funções                                                          | Descrição                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Especifica ou retorna sinalizadores que controlam o acesso ao armazenamento da [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA).<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Especifica ou retorna o nome do repositório de autoridade de certificação.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Especifica ou retorna o tipo do repositório identificado pela propriedade **CAStoreName** .<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Especifica ou retorna um sinalizador que determina o caminho do repositório pessoal.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Especifica ou retorna o nome do repositório pessoal.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Especifica ou retorna o tipo do repositório pessoal.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Especifica ou retorna um sinalizador que determina o caminho do repositório de solicitações.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Especifica ou retorna o nome do repositório de solicitações.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Especifica ou retorna o tipo do repositório de solicitações.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Especifica ou retorna um sinalizador que determina o caminho do repositório raiz.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Especifica ou retorna o nome do repositório raiz.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Especifica ou retorna o tipo do repositório raiz.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Especifica o identificador do repositório de autoridade de certificação.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Especifica o identificador do repositório pessoal.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Especifica o identificador do repositório de solicitações.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Especifica o identificador do repositório raiz.<br/>                                                                                                                                                   |



 

CertEnroll.dll não exporta a funcionalidade que permite especificar ou recuperar valores de propriedade de armazenamento ou copiar certificados para repositórios específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

