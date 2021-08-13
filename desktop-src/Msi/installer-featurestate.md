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
ms.openlocfilehash: 989abe860848b943e77b02910e9760f8fcaecc97fd8a2634f8147605577613d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631270"
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
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




