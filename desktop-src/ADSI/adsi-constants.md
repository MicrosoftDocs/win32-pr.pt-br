---
title: Constantes ADSI
description: A tabela a seguir lista as constantes definidas e usadas nas interfaces de serviço do Active Directory (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634897"
---
# <a name="adsi-constants"></a>Constantes ADSI

A tabela a seguir lista as constantes definidas e usadas nas interfaces de serviço do Active Directory (ADSI).



| Constante de ADSI                      | Valor                                   | Descrição                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_INITCREDENTIALS ext \_ ADS**      | 1                                       | Um código de controle que indica que os dados personalizados fornecidos para o método [**IADsExtension:: opere**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contêm credenciais de usuário.                                                     |
| **inicialização de ext de anúncios \_ \_ \_ concluída** | 2                                       | Um código de controle usado com [**IADsExtension:: Opera**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que as extensões podem executar qualquer inicialização necessária, dependendo dos recursos com suporte pelo objeto pai. |
| **\_MAXEXTDISPID ext \_ ADS**         | 16777215                                | O DISPID mais alto que um objeto de extensão pode usar para seus métodos e propriedades.                                                                                                                                   |
| **\_MINEXTDISPID ext \_ ADS**         | 1                                       | O DISPID mais baixo que um objeto de extensão pode usar para seus métodos e propriedades.                                                                                                                                    |
| **\_resposta VLV de anúncios \_**             | L "fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Usado com o método [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar os metadados de pesquisa VLV. Para obter mais informações, consulte [como Pesquisar usando a VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Usado para trabalhar com o provedor de OLE DB.                                                                                                                                                                           |



 

 

 




