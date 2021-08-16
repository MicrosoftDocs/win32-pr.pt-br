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
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094902"
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

Tipo: **ppidl \***

No retorno, contém o endereço de um ponteiro para uma lista de identificadores de item (PIDL) que identifica a pasta pai. O parâmetro *LPITEMIDLIST* pode se referir a um objeto em qualquer nível abaixo da pasta pai na hierarquia de namespace e, portanto, pode ser um ponteiro de vários níveis para um **PIDL** relativo à pasta pai.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

o método **ISearchItem:: GetParentFolder** tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usado.

para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchItem**](-search-isearchitem.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**linkid**](-search-linktype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Redistribuível<br/>          | Windows Pesquisa de desktop (WDS) 3,0<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
