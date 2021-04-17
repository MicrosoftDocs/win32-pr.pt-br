---
description: A propriedade Patchproperty Obtém informações sobre um patch específico aplicado a uma instância específica do produto. Essa propriedade chama MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Método patch. Patchproperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748145"
---
# <a name="patchpatchproperty-method"></a>Método patch. Patchproperty

A propriedade **patchproperty** Obtém informações sobre um patch específico aplicado a uma instância específica do produto. Essa propriedade chama [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

## <a name="syntax"></a>Sintaxe


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szProperty* 
</dt> <dd>

O parâmetro *szProperty* pode ser um dos valores a seguir.



| Nome          | Significado                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Obtenha o arquivo de patch armazenado em cache usado pelo produto.                                                                                                                                                                                                                                                                               |
| Transformações    | Obtenha o conjunto de transformações de patch aplicadas ao produto pela última instalação do patch. Esse valor pode não estar disponível para aplicativos não gerenciados por usuário se o usuário não estiver conectado ao computador.                                                                                                                     |
| InstallDate   | Obtenha a data em que o patch foi aplicado ao produto.                                                                                                                                                                                                                                                                      |
| Desinstalado | Retorna "1" se o patch for marcado como possível para ser desinstalado do produto. Nesse caso, o instalador ainda poderá bloquear a desinstalação se esse patch for exigido por outro patch que não pode ser desinstalado.                                                                                                          |
| Estado         | Retorna "1" se esse patch estiver aplicado no momento ao produto. Retorna "2" se esse patch tiver sido substituído por outro patch. Retorna "4" se esse patch tiver sido tornado obsoleto por outro patch. Esses valores correspondem às constantes usadas pelo parâmetro *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa). |
| DisplayName   | Obtenha o nome de exibição registrado para o patch. Para patches que não incluem a propriedade DisplayName na tabela [MsiPatchMetaData](msipatchmetadata-table.md) , o nome de exibição retornado é uma cadeia de caracteres vazia ("").                                                                                                      |
| MoreInfoURL   | Obtenha a URL de informações de suporte registradas para o patch. Para patches que não incluem a propriedade MoreInfoURL na tabela [MsiPatchMetaData](msipatchmetadata-table.md) , a URL de informações de suporte retornada é uma cadeia de caracteres vazia ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

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

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




