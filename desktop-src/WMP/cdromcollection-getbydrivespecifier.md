---
title: Método cdromCollection. getByDriveSpecifier
description: O método getByDriveSpecifier recupera o objeto de cdrom associado a uma letra de unidade específica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- método getByDriveSpecifier Windows Media Player
- método getByDriveSpecifier Windows Media Player, classe cdromCollection
- Classe cdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794503"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Método cdromCollection. getByDriveSpecifier

O método **getByDriveSpecifier** recupera o objeto de **cdrom** associado a uma letra de unidade específica.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*driveSpecifier* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém a letra da unidade seguida por um caractere de dois-pontos (":").

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto de **cdrom** .

## <a name="remarks"></a>Comentários

As letras da unidade devem ser fornecidas no formato *x*:, em que *X* representa a letra da unidade.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *cdromCollection*. **getByDriveSpecifier** para recuperar o objeto de **cdrom** que corresponde a uma letra de unidade fornecida pelo usuário. Um elemento de texto HTML foi criado, com NAME = "MyText", para entrada do usuário. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdrom. ejeção**](cdrom-eject.md)
</dt> <dt>

[**Objeto cdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





