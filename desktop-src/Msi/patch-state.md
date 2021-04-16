---
description: A propriedade State retorna o estado de instalação dessa instância do patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Propriedade patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751430"
---
# <a name="patchstate-property"></a>Propriedade patch. State

A propriedade **State** retorna o estado de instalação dessa instância do patch.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa propriedade retorna um dos valores a seguir.



| Estado da instalação        | Significado                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ aplicado    | O patch é aplicado a esta instância de produto.                   |
| MSIPATCHSTATE \_ substituído | O patch é aplicado a esta instância do produto, mas está substituído. |
| MSIPATCHSTATE \_ obsoleto  | O patch é aplicado nesta instância do produto, mas obsoleto.      |



 

Esse método pode retornar \_ um patch desconhecido de erro \_ , se o objeto [**patch**](patch-object.md) for inicializado com uma cadeia de caracteres vazia para *ProductCode*.

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

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




