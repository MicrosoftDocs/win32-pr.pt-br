---
description: O método RemovePatches remove um ou mais patches para produtos qualificados para receber o patch. O método RemovePatches chama MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Método Installer. RemovePatches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894026"
---
# <a name="installerremovepatches-method"></a>Método Installer. RemovePatches

O método **RemovePatches** remove um ou mais patches para produtos qualificados para receber o patch. O método **RemovePatches** chama [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

## <a name="syntax"></a>Sintaxe


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PATCHLIST* 
</dt> <dd>

Uma cadeia de caracteres que contém uma lista delimitada por ponto e vírgula de patches a serem removidos. Cada patch pode ser representado pelo caminho completo para o pacote de patch ou por GUID de patch. Este parâmetro é necessário.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Uma cadeia de caracteres com o GUID do produto do qual os patches devem ser removidos. Este parâmetro é necessário.

</dd> <dt>

*Desinstaletype* 
</dt> <dd>

Um valor inteiro que especifica o tipo de remoção de patch. Esse parâmetro deve ser **msiInstallTypeSingleInstance**.

</dd> <dt>

*PropertyList* 
</dt> <dd>

Uma cadeia de caracteres que especifica os pares de propriedade = valor a serem incluídos. Esse parâmetro é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Consulte [desinstalando patches](uninstalling-patches.md) para obter um exemplo que demonstra como um aplicativo pode remover um patch de todos os produtos que estão disponíveis para o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Desinstalando patches](uninstalling-patches.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




