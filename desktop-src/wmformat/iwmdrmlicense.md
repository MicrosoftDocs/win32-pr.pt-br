---
title: Interface IWMDRMLicense
description: A interface IWMDRMLicense representa uma lista de uma ou mais licenças.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Formato de mídia do Windows da interface IWMDRMLicense
- Formato de mídia do Windows da interface IWMDRMLicense, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38aadbda7a0ab6e899e4100adb5ff03873a4dd683fcb8f5893c506033545d558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847123"
---
# <a name="iwmdrmlicense-interface"></a>Interface IWMDRMLicense

A interface **IWMDRMLicense** representa uma lista de uma ou mais licenças.

## <a name="members"></a>Membros

A interface **IWMDRMLicense** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicense** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMLicense** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Persiste**](iwmdrmlicense-canpersist.md)                                           | Consulta se a licença pode persistir em um repositório de licenças local.<br/>                                                                                                                                               |
| [**Createdescriptografar**](iwmdrmlicense-createdecryptor.md)                                 | Cria um objeto de descriptografador usando as configurações da licença atual.<br/>                                                                                                                                                   |
| [**Createcriptografer**](iwmdrmlicense-createencryptor.md)                                 | Cria um objeto de criptografador usando as configurações da licença atual.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Cria um objeto de descriptografia seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Recupera todas as restrições de vídeo analógicas definidas na licença atual.<br/>                                                                                                                                                     |
| [**Getinclusõeslist**](iwmdrmlicense-getinclusionlist.md)                               | Recupera a lista de inclusão inteira da licença atual ou da cadeia de licença.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Recupera a licença como dados de linguagem XML (XML) ou XMR (direitos de mídia extensível).<br/>                                                                                                                        |
| [**Getlicenciadoproperty**](iwmdrmlicense-getlicenseproperty.md)                           | Recupera uma propriedade da licença atual.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Carrega as informações sobre a próxima licença na lista.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Salva a licença atual do repositório temporário no armazenamento de licença local permanente.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Redefine a lista de licenças para seu estado original.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

