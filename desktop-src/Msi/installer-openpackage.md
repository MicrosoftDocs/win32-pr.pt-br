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
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747543"
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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **OpenPackage** pode aceitar o identificador de banco de dados diretamente em vez da cadeia de caracteres para o caminho do pacote.

Observe que apenas um objeto de [**sessão**](session-object.md) pode ser aberto por um único processo. **OpenPackage** não pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.

Um objeto de [**sessão**](session-object.md) seguro ignora o estado atual do computador ao abrir o pacote e impede alterações no estado atual do computador. Para obter mais informações, consulte [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




