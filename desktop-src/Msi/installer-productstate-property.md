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
ms.openlocfilehash: c19a712c4838905296026a2a0bea4c9e1abc1c49465a854692dd603734e0bd89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763616"
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

## <a name="return-value"></a>Valor retornado

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
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




