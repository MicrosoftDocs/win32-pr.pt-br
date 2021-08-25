---
title: Método CdromCollection.getByDriveSpecifier
description: O método getByDriveSpecifier recupera o objeto Cdrom associado a uma letra de unidade específica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Método getByDriveSpecifier Windows Media Player
- Método getByDriveSpecifier Windows Media Player classe , CdromCollection
- Classe CdromCollection Windows Media Player , método getByDriveSpecifier
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
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864086"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Método CdromCollection.getByDriveSpecifier

O **método getByDriveSpecifier** recupera o **objeto Cdrom** associado a uma letra de unidade específica.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*driveSpecifier* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém a letra da unidade seguida por um caractere de dois-pontos (":").

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Cdrom.**

## <a name="remarks"></a>Comentários

As letras da unidade devem ser fornecidas no formato *X*:, em que *X* representa a letra da unidade.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir *usa CdromCollection*. **getByDriveSpecifier** para recuperar o **objeto Cdrom** que corresponde a uma letra da unidade fornecida pelo usuário. Um elemento de texto HTML foi criado, com NAME = "MyText", para entrada do usuário. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdrom.ejetar**](cdrom-eject.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





