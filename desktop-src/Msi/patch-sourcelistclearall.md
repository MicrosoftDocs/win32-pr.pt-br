---
description: O método SourceListClearAll do objeto Patch limpa a lista de origem completa de todas as fontes do tipo especificado para um patch. Aceita Tipo como um parâmetro. Esse método chama MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Método Patch.SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942296"
---
# <a name="patchsourcelistclearall-method"></a>Método Patch.SourceListClearAll

O **método SourceListClearAll** do objeto [**Patch**](patch-object.md) limpa a lista de origem completa de todas as fontes do tipo especificado para um patch. Aceita *Tipo* como um parâmetro. Esse método chama [**MsiSourceListClearAllEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)

## <a name="syntax"></a>Sintaxe


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* 
</dt> <dd>

O tipo de tipo de origem, como rede, URL ou mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador 3.0 ou posterior no Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch é definido como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




