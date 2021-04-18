---
description: O método ExtractPatchXMLData do objeto do instalador extrai informações de um patch como uma cadeia de caracteres XML. As informações podem ser usadas para determinar se o patch se aplica a um sistema de destino. Esse método chama MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Método Installer. ExtractPatchXMLData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752642"
---
# <a name="installerextractpatchxmldata-method"></a>Método Installer. ExtractPatchXMLData

O método **ExtractPatchXMLData** do objeto do [**instalador**](installer-object.md) extrai informações de um patch como uma cadeia de caracteres XML. As informações podem ser usadas para determinar se o patch se aplica a um sistema de destino. Esse método chama [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PatchPath* 
</dt> <dd>

Caminho completo do patch do qual as informações de aplicabilidade serão extraídas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




