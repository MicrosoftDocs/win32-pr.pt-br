---
description: A propriedade Featurestate somente leitura retorna o estado instalado de um recurso.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Propriedade Installer. Featurestate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747972"
---
# <a name="installerfeaturestate-property"></a>Propriedade Installer. Featurestate

A propriedade **featurestate** somente leitura retorna o estado instalado de um recurso.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa propriedade retorna um dos valores a seguir.



| Valor                     | Descrição                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | O recurso não está instalado.                    |
| msiInstallStateAdvertised | O recurso é anunciado.                       |
| msiInstallStateLocal      | O recurso é instalado para ser executado localmente.         |
| msiInstallStateSource     | O recurso é instalado para ser executado da origem.     |
| msiInstallStateInvalidArg | Um parâmetro inválido foi passado para a função. |
| msiInstallStateUnknown    | O código do produto ou a ID do recurso é desconhecido.       |
| msiInstallStateBadConfig  | Os dados de configuração estão corrompidos.               |



 

 

A propriedade **featurestate** não valida se o recurso está acessível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




