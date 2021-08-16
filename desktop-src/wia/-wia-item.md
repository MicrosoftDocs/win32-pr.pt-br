---
description: Windows Dispositivos de hardware WIA (Aquisição de Imagem) são representados como árvores hierárquicas de objetos Item. O item raiz nessa árvore representa o próprio dispositivo, enquanto os itens filho representam imagens, pastas ou pastas de varredura.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Objeto item
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
ms.openlocfilehash: 2b5b32603f334148fede3bc2866367817fd3dcd5ab33aaa40bab84fe3cf49624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208929"
---
# <a name="item-object"></a>Objeto item

Windows Dispositivos de hardware WIA (Aquisição de Imagem) são representados como árvores hierárquicas de **objetos Item.** O item raiz nessa árvore representa o próprio dispositivo, enquanto os itens filho representam imagens, pastas ou pastas de varredura.

Use o **objeto Item** para transferir dados para um arquivo, para navegar na árvore de itens de um dispositivo específico ou para recuperar informações sobre uma imagem ou um dispositivo.

## <a name="members"></a>Membros

O **objeto Item** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto Item** tem esses métodos.



| Método                                                         | Descrição                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | O [**método GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) do **objeto Item** exibe uma caixa de diálogo que permite que um usuário selecione imagens e áudio para transferir de um dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | O [**método GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) do **objeto Item** usa a ID de uma propriedade de item para retornar seu valor.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | O [**método TakePicture**](-wia-iwiadispatchitem-takepicture.md) do **objeto Item** faz com que um dispositivo de câmera digital tire uma foto e retorna um objeto **Item** que representa a imagem resultante. Esse método se aplica somente a dispositivos de câmera digital.<br/> |
| [**Transferência**](-wia-iwiadispatchitem-transfer.md)             | O [**método**](-wia-iwiadispatchitem-transfer.md) Transfer do **objeto Item** transfere dados de um dispositivo para um arquivo. Esse método se aplica somente a itens de tipo de dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Propriedades

O **objeto Item** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso          | Descrição                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Somente leitura<br/> | A [**propriedade Children**](-wia-iwiadispatchitem-children.md) do objeto **Item** recupera uma coleção de **objetos Item.** Os itens nesta coleção representam itens que são filhos diretos desse item na árvore hierárquica. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Somente leitura<br/> | Recupera o status de conexão do dispositivo. Essa propriedade se aplica somente a itens do tipo dispositivo (itens raiz). Os valores possíveis são "conectados", "desconectados" ou **NULL** (se essa propriedade não se aplicar ao item). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Somente leitura<br/> | Recupera a versão de firmware do dispositivo. Essa propriedade se aplica somente a itens do tipo dispositivo (itens raiz). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Somente leitura<br/> | Recupera o nome completo do item como ele aparece na interface do usuário. <br/>                                                                                                                                                                                    |
| [**Altura**](-wia-iwiadispatchitem-height.md)<br/>                   | Somente leitura<br/> | A altura, em pixels, do item. <br/>                                                                                                                                                                                                             |
| [**Itemtype**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Somente leitura<br/> | O tipo desse item. <br/>                                                                                                                                                                                                                          |
| [**Nome**](-wia-iwiadispatchitem-name.md)<br/>                       | Somente leitura<br/> | O nome do item como ele aparece na interface do usuário. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Somente leitura<br/> | A altura, em pixels, das imagens produzidas por essa câmera digital. Aplica-se somente a câmeras digitais. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Somente leitura<br/> | A largura, em pixels, das imagens produzidas por essa câmera digital. Aplica-se somente a câmeras digitais. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Somente leitura<br/> | A altura, em pixels, da imagem em miniatura. Essa propriedade retornará -1 se esse item não tiver suporte para miniaturas. <br/>                                                                                                                               |
| [**Thumbnail**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Somente leitura<br/> | O caminho e o nome do arquivo da imagem em miniatura. Essa propriedade será **NULL** se o item não tiver suporte para miniaturas ou se um caminho não puder ser criado. <br/>                                                                                                  |
| [**Thumbwidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Somente leitura<br/> | A largura, em pixels, da imagem em miniatura. Essa propriedade retornará -1 se esse item não tiver suporte para miniaturas. <br/>                                                                                                                                |
| [**Tempo**](-wia-iwiadispatchitem-time.md)<br/>                       | Somente leitura<br/> | A hora atual. Aplica-se somente a dispositivos. <br/>                                                                                                                                                                                                      |
| [**Largura**](-wia-iwiadispatchitem-width.md)<br/>                     | Somente leitura<br/> | A largura, em pixels, do item. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

### <a name="creationaccess-functions"></a>Funções \\ de acesso de criação

Use qualquer um dos seguintes para recuperar uma referência ao objeto :



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Criar**](-wia-iwiadeviceinfo-create.md)

[**Criar**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |



 

 




