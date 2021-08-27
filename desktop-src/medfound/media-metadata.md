---
description: Metadados de mídia
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadados de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef9f8a852bbce2dfb8d38a5883acc219cde8019
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477081"
---
# <a name="media-metadata"></a>Metadados de mídia

Os arquivos de mídia contêm propriedades que descrevem o conteúdo do arquivo. Em Microsoft Media Foundation, essas propriedades podem ser categorizadas da seguinte forma:

-    Atributos de tipo de mídia especificam os parâmetros de codificação, como o algoritmo de codificação (subtipo de mídia), o tamanho do quadro de vídeo, a taxa de quadros de vídeo, a taxa de bits de áudio e a taxa de amostra de áudio. Para obter mais informações sobre atributos de tipo de mídia, consulte [Tipos de mídia](media-types.md).
-   **Os metadados** contêm informações descritivas para o conteúdo da mídia, como título, artista, compositor e gênero. Os metadados também podem descrever parâmetros de codificação. Pode ser mais rápido acessar essas informações por meio de metadados do que por meio de atributos de tipo de mídia.
-   **As propriedades drm** contêm informações sobre restrições de uso. Atualmente, Media Foundation dá suporte a propriedades DRM por meio de metadados, com exceção da **propriedade \_ \_ IsProtected do DRM PKEY.**

Há duas maneiras de ler metadados Media Foundation:

-   A [**interface IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation metadados da versão 1).
-   A interface Windows [**Shell IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (metadados do Shell).

Os metadados do Shell pertencem não apenas a arquivos de mídia, mas a uma gama muito maior de arquivos no sistema.

A tabela a seguir compara os recursos e as limitações de cada API de metadados.




| Media Foundation metadados v1 | Metadados do Shell | 
|------------------------------|----------------|
| Requer Windows Vista ou posterior. | Requer Windows 7.<blockquote>[!Note]<br />Em geral, os metadados do shell não exigem Windows 7, mas Media Foundation não suportam metadados do Shell antes Windows 7.</blockquote><br /> | 
| As propriedades não são compatíveis com o sistema de propriedades do Shell. | As propriedades são compatíveis com o sistema de propriedades do Shell. | 
| As propriedades podem ser aplicadas a todo o arquivo ou no nível do fluxo. | Há suporte apenas para propriedades de nível de arquivo. Não há suporte para propriedades de nível de fluxo. | 
| As propriedades podem ter valores em vários idiomas. | Não há suporte para valores em vários idiomas. | 
| As chaves de propriedade são cadeias de caracteres largos. | As chaves de propriedade <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>são valores PROPERTYKEY.</strong></a> | 
| Os valores de propriedade <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>são valores PROPVARIANT.</strong></a> | Os valores de propriedade <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>são valores PROPVARIANT.</strong></a> | 




 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Provedores de metadados do Shell](shell-metadata-providers.md)<br/>                       | A partir Windows 7, Media Foundation expõe metadados por meio da interface [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)<br/> |
| [Propriedades de metadados para Arquivos de mídia](metadata-properties-for-media-files.md)<br/> | Este tópico lista as propriedades de metadados mais comuns para arquivos de mídia.<br/>                                                           |
| [Provedores de metadados no Windows Vista](metadata-providers-in-windows-vista.md)<br/> | No Windows Vista, Media Foundation expõe metadados por meio da interface [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)<br/>                   |



 

Se você estiver implementando uma fonte de mídia personalizada e quiser expor metadados do Shell, consulte Provedores de [metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
