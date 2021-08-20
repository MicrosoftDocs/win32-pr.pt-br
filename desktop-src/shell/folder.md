---
description: Representa uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objeto de pasta (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032614"
---
# <a name="folder-object"></a>Objeto de pasta

Representa uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a pasta.

## <a name="members"></a>Membros

O objeto **Folder** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Folder** tem esses métodos.



| Método                                      | Descrição                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copia um item ou itens para uma pasta.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Recupera detalhes sobre um item em uma pasta. Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.<br/> |
| [**Itens**](folder-items.md)               | Recupera um objeto [**FolderItems**](folderitems.md) que representa a coleção de itens na pasta.<br/>    |
| [**MoveHere**](folder-movehere.md)         | Move um item ou itens para esta pasta.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Cria uma nova pasta.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Cria e retorna um objeto [**FolderItem**](folderitem.md) que representa um item especificado.<br/>                 |



 

### <a name="properties"></a>Propriedades

O objeto **Folder** tem essas propriedades.



| Propriedade                                               | Tipo de acesso          | Descrição                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Aplicativo**](folder-application.md)<br/>   | Somente leitura<br/> | Contém o objeto de aplicativo da pasta.<br/> |
| [**Pai**](folder-parent.md)<br/>             | Somente leitura<br/> | Não implementado.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Somente leitura<br/> | Contém o objeto da **pasta** pai.<br/>    |
| [**Título**](folder-title.md)<br/>               | Somente leitura<br/> | Contém o título da pasta.<br/>         |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL). Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                 |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




