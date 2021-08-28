---
description: O método OpenPackage do objeto do instalador abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação, retornando um objeto de sessão.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Método Installer. OpenPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc3e96fe55e37a55d5601a0a2d702e6a98582879bf2cff65ee52b5ca6bdc1772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388146"
---
# <a name="installeropenpackage-method"></a>Método Installer. OpenPackage

O método **OpenPackage** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação, retornando um objeto de [**sessão**](session-object.md) .

## <a name="syntax"></a>Sintaxe


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Cadeia de caracteres necessária que contém o nome do caminho do pacote.

</dd> <dt>

*options* 
</dt> <dd>

Um valor inteiro opcional que especifica se **OpenPackage** deve ou não ignorar o estado atual do computador ao criar o objeto de sessão. Nenhum valor ou um valor de 0 para opções usa como padrão o comportamento original. Quando as opções são 1, o método **OpenPackage** ignora o estado atual do computador ao abrir o pacote. Um valor de 1 impede alterações no estado atual do computador. Para obter mais informações, consulte [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **OpenPackage** pode aceitar o identificador de banco de dados diretamente em vez da cadeia de caracteres para o caminho do pacote.

Observe que apenas um objeto de [**sessão**](session-object.md) pode ser aberto por um único processo. **OpenPackage** não pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.

Um objeto de [**sessão**](session-object.md) seguro ignora o estado atual do computador ao abrir o pacote e impede alterações no estado atual do computador. Para obter mais informações, consulte [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




