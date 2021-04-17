---
description: O método ForceSourceListResolution do objeto instalador força a Windows Installer a Pesquisar a lista de origem em busca de uma origem de produto válida.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Método Installer. ForceSourceListResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752850"
---
# <a name="installerforcesourcelistresolution-method"></a>Método Installer. ForceSourceListResolution

O método **ForceSourceListResolution** do objeto [**instalador**](installer-object.md) força o instalador a Pesquisar a lista de origem para uma fonte de produto válida na próxima vez que uma fonte for necessária, como quando o instalador executa uma instalação ou reinstalação, ou quando precisa do caminho para um conjunto de componentes ser executado da origem.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o código do produto.

</dd> <dt>

*Usuário* 
</dt> <dd>

Nome de usuário para instalação por usuário; Cadeia de caracteres nula ou vazia para instalação por máquina.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




