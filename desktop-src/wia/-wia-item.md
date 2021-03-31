---
description: Os dispositivos de hardware da aquisição de imagens do Windows (WIA) são representados como árvores hierárquicas de objetos de item. O item raiz nessa árvore representa o próprio dispositivo, enquanto os itens filho representam imagens, pastas ou ambientes de verificação.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Objeto Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647486"
---
# <a name="item-object"></a>Objeto Item

Os dispositivos de hardware da aquisição de imagens do Windows (WIA) são representados como árvores hierárquicas de objetos de **Item** . O item raiz nessa árvore representa o próprio dispositivo, enquanto os itens filho representam imagens, pastas ou ambientes de verificação.

Use o objeto **Item** para transferir dados para um arquivo, para navegar na árvore de itens de um determinado dispositivo ou para recuperar informações sobre uma imagem ou um dispositivo.

## <a name="members"></a>Membros

O objeto **Item** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Item** tem esses métodos.



| Método                                                         | Descrição                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | O método [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) do objeto **Item** exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | O método [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) do objeto **Item** usa a ID de uma propriedade item para retornar seu valor.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | O método [**TakePicture**](-wia-iwiadispatchitem-takepicture.md) do objeto **Item** faz com que um dispositivo de câmera digital pegue uma imagem e retorna um objeto **Item** que representa a imagem resultante. Esse método se aplica somente a dispositivos de câmera digital.<br/> |
| [**Transferência**](-wia-iwiadispatchitem-transfer.md)             | O método de [**transferência**](-wia-iwiadispatchitem-transfer.md) do objeto **Item** transfere dados de um dispositivo para um arquivo. Esse método aplica-se somente a itens de tipo de dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Propriedades

O objeto **Item** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso          | Descrição                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Somente leitura<br/> | A propriedade [**Children**](-wia-iwiadispatchitem-children.md) do objeto **Item** recupera uma coleção de objetos **Item** . Os itens nesta coleção representam itens que são filhos diretos deste item na árvore hierárquica. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Somente leitura<br/> | Recupera o status de conexão do dispositivo. Essa propriedade só se aplica a itens do tipo dispositivo (itens raiz). Os valores possíveis são "Connected", "Disconnected" ou **NULL** (se essa propriedade não se aplicar ao item). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Somente leitura<br/> | Recupera a versão do firmware do dispositivo. Essa propriedade só se aplica a itens do tipo dispositivo (itens raiz). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Somente leitura<br/> | Recupera o nome completo do item como ele aparece na interface do usuário. <br/>                                                                                                                                                                                    |
| [**Altura**](-wia-iwiadispatchitem-height.md)<br/>                   | Somente leitura<br/> | A altura, em pixels, do item. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Somente leitura<br/> | O tipo deste item. <br/>                                                                                                                                                                                                                          |
| [**Nome**](-wia-iwiadispatchitem-name.md)<br/>                       | Somente leitura<br/> | O nome do item como ele aparece na interface do usuário. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Somente leitura<br/> | A altura, em pixels, das imagens produzidas por essa câmera digital. Aplica-se somente a câmeras digitais. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Somente leitura<br/> | A largura, em pixels, das imagens produzidas por essa câmera digital. Aplica-se somente a câmeras digitais. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Somente leitura<br/> | A altura, em pixels, da imagem em miniatura. Essa propriedade retornará-1 se este item não oferecer suporte a miniaturas. <br/>                                                                                                                               |
| [**Thumbnail**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Somente leitura<br/> | O caminho e o nome do arquivo da imagem em miniatura. Essa propriedade será **nula** se o item não oferecer suporte a miniaturas ou se um caminho não puder ser compilado. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Somente leitura<br/> | A largura, em pixels, da imagem em miniatura. Essa propriedade retornará-1 se este item não oferecer suporte a miniaturas. <br/>                                                                                                                                |
| [**Momento**](-wia-iwiadispatchitem-time.md)<br/>                       | Somente leitura<br/> | A hora atual. Aplica-se somente a dispositivos. <br/>                                                                                                                                                                                                      |
| [**Largura**](-wia-iwiadispatchitem-width.md)<br/>                     | Somente leitura<br/> | A largura, em pixels, do item. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

### <a name="creationaccess-functions"></a>Criar \\ funções de acesso

Use qualquer um dos seguintes para recuperar uma referência ao objeto:



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Criada**](-wia-iwiadeviceinfo-create.md)

[**Criar**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




