---
description: Remove uma fonte de rede ou URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Método patch. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752032"
---
# <a name="patchsourcelistclearsource-method"></a>Método patch. SourceListClearSource

O método **SourceListClearSource** remove uma fonte de rede ou URL. Esse método chama [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).

## <a name="syntax"></a>Sintaxe


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de fonte a ser removida.

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

**\_rede MSISOURCETYPE**
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

**URL do MSISOURCETYPE \_**
</dt> </dl> </dd> <dt>

*SourcePath* 
</dt> <dd>

Caminho para a origem a ser removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




