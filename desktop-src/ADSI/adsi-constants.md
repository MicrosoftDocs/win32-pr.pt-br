---
title: Constantes ADSI
description: A tabela a seguir lista as constantes definidas e usadas em ADSI (Interfaces de Serviço do Active Directory).
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
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023914"
---
# <a name="adsi-constants"></a>Constantes ADSI

A tabela a seguir lista as constantes definidas e usadas em ADSI (Interfaces de Serviço do Active Directory).



| Constante ADSI                      | Valor                                   | Descrição                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ EXT \_ INITCREDENTIALS**      | 1                                       | Um código de controle que indica que os dados personalizados fornecidos para o método [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contêm credenciais de usuário.                                                     |
| **ADS \_ EXT \_ INITIALIZE \_ COMPLETE** | 2                                       | Um código de controle usado com [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que as extensões podem executar qualquer inicialização necessária, dependendo dos recursos com suporte pelo objeto pai. |
| **ADS \_ EXT \_ MAXEXTDISPID**         | 16777215                                | O DISPID mais alto que um objeto de extensão pode usar para seus métodos e propriedades.                                                                                                                                   |
| **ADS \_ EXT \_ MINEXTDISPID**         | 1                                       | O DISPID mais baixo que um objeto de extensão pode usar para seus métodos e propriedades.                                                                                                                                    |
| **RESPOSTA \_ DO ADS \_ VLV**             | L"fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Usado com o [**método IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar metadados de pesquisa VLV. Para obter mais informações, [consulte How to Search Using VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Usado para trabalhar com o provedor OLE DB dados.                                                                                                                                                                           |



 

 

 




