---
description: Requisitos para recursos
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisitos para recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170677"
---
# <a name="requirements-for-resources"></a>Requisitos para recursos

Os dispositivos portáteis do Windows definem as seguintes categorias de recursos como valores de **PROPERTYKEY** . Esses valores são usados para descrever recursos individuais em um objeto. O membro *pid* da chave de propriedade pode ser diferente para descrever recursos diferentes do mesmo tipo para todos os tipos, exceto o **\_ \_ padrão de recursos WPD**, que pode descrever apenas um recurso. A página descrição vinculada para cada tipo de recurso lista os atributos suportados por esse recurso.



| PROPERTYKEY do recurso                                                | Descrição                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_padrão de recursos WPD \_**](wpd-resource-default.md)              | Especifica o arquivo inteiro por trás do objeto. Esse é o único recurso necessário para qualquer objeto com um recurso. |
| [**\_arte do \_ álbum de recursos WPD \_**](wpd-resource-album-art.md)         | Especifica uma imagem que representa a arte-final do álbum do objeto.                                           |
| [**\_clipe de \_ áudio de recursos WPD \_**](wpd-resource-audio-clip.md)       | Especifica um clipe de áudio para o objeto.                                                                        |
| [**\_foto de \_ contato de recursos WPD \_**](wpd-resource-contact-photo.md) | Especifica uma imagem que representa uma foto do indivíduo referenciado no objeto de contato.                |
| [**recurso de WPD \_ \_ genérico**](wpd-resource-generic.md)              | Um recurso genérico de tipo de dados indefinido. Isso deve ser tratado como uma matriz de bytes.                             |
| [**\_ícone de recurso WPD \_**](wpd-resource-icon.md)                    | Um ícone.                                                                                                       |
| [**\_miniatura do recurso WPD \_**](wpd-resource-thumbnail.md)          | Uma imagem em miniatura.                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



