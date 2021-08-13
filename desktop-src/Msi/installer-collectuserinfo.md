---
description: O método CollectUserInfo do objeto Installer invoca uma sequência de assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Método Installer.CollectUserInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 255f9c5bfbd9f7ed476314e8ac1c9ed58568c083b8f6ea7704bbe5cfef15b769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632913"
---
# <a name="installercollectuserinfo-method"></a>Método Installer.CollectUserInfo

O **método CollectUserInfo** do objeto [**Installer**](installer-object.md) invoca uma sequência de assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o [**código do produto.**](productcode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um aplicativo deve chamar o **método CollectUserInfo** na primeira vez que for executado. O **método CollectUserInfo** abre o pacote de instalação do produto e invoca uma sequência de assistente de interface do usuário autoral que coleta informações do usuário. Após a conclusão da sequência de assistente, as informações do usuário coletadas são registradas. A [**propriedade UILevel**](installer-uilevel.md) deve ser definida como msiUILevelFull porque essa API requer uma interface do usuário autorada.

O **método CollectUserInfo** invoca a [caixa de diálogo FirstRun](firstrun-dialog.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




