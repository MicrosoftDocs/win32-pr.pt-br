---
description: A propriedade Productstate é uma propriedade somente leitura que retorna as informações de estado de instalação de um produto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Método de Propriedade Installer. Productstate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748153"
---
# <a name="installerproductstate-property-method"></a>Método de Propriedade Installer. Productstate

A **Propriedade productstate** é uma propriedade somente leitura que retorna as informações de estado de instalação de um produto.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Product* 
</dt> <dd>

Especifica o código do produto do produto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Retorna um dos valores mostrados na tabela a seguir.



| Estado de instalação        | Descrição                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | O produto está instalado para um usuário diferente.   |
| msiInstallStateDefault    | O produto está instalado para o usuário atual.   |
| msiInstallStateAdvertised | O produto é anunciado, mas não está instalado.     |
| msiInstallStateInvalidArg | Um parâmetro inválido foi passado para a função. |
| msiInstallStateUnknown    | O produto não está anunciado nem instalado. |
| msiInstallStateBadConfig  | Os dados de configuração estão corrompidos.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




