---
description: O método CollectUserInfo do objeto do instalador invoca uma sequência do assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Método Installer. CollectUserInfo
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
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750235"
---
# <a name="installercollectuserinfo-method"></a>Método Installer. CollectUserInfo

O método **CollectUserInfo** do objeto do [**instalador**](installer-object.md) invoca uma sequência do assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.

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

Especifica o [**código do produto**](productcode.md) do produto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um aplicativo deve chamar o método **CollectUserInfo** na primeira vez em que for executado. O método **CollectUserInfo** abre o pacote de instalação do produto e invoca uma sequência de assistente de interface de usuário criada que coleta informações do usuário. Após a conclusão da sequência do assistente, as informações de usuário coletadas são registradas. A propriedade [**UILevel**](installer-uilevel.md) deve ser definida como msiUILevelFull porque essa API requer uma interface de usuário criada.

O método **CollectUserInfo** invoca a [caixa de diálogo FirstRun](firstrun-dialog.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




