---
description: Obtém o objeto ISearchItem se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Método ISearchItem:: GetParentFolder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793252"
---
# <a name="isearchitemgetparentfolder-method"></a>Método ISearchItem:: GetParentFolder

Obtém o objeto [**ISearchItem**](-search-isearchitem.md) se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IShellFolder* \[ fora\]
</dt> <dd>

Tipo: **ppShellFolder \* \***

No retorno, contém o endereço de um ponteiro para a pasta que contém a URL atual. A [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) é exposta por todos os objetos de pasta de namespace do Shell, e seus métodos são usados para gerenciar pastas.

</dd> <dt>

*LPITEMIDLIST* \[ fora\]
</dt> <dd>

Tipo: **ppidl \** _

No retorno, contém o endereço de um ponteiro para uma lista de identificadores de item (PIDL) que identifica a pasta pai. O parâmetro _LPITEMIDLIST * pode se referir a um objeto em qualquer nível abaixo da pasta pai na hierarquia de namespace e, portanto, pode ser um ponteiro de vários níveis para um **PIDL** relativo à pasta pai.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método **ISearchItem:: GetParentFolder** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.

Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchItem**](-search-isearchitem.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
