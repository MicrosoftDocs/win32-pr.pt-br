---
description: A propriedade MSIRMSHUTDOWN determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propriedade MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780948"
---
# <a name="msirmshutdown-property"></a>Propriedade MSIRMSHUTDOWN

A propriedade **MSIRMSHUTDOWN** determina como os aplicativos ou serviços que estão usando atualmente arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.

## <a name="value"></a>Valor



| Valor                                                                        | Significado                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Os processos ou serviços que estão usando arquivos afetados pela atualização estão desligados.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Os processos ou serviços que estão usando arquivos afetados pela atualização e que não respondem ao [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md)são forçados a desligar.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Os processos ou serviços que estão usando arquivos afetados pela atualização serão desligados somente se tiverem sido registrados para uma reinicialização. Se algum processo ou serviço não tiver sido registrado para uma reinicialização, não haverá processos ou serviços desligados.<br/> |



 

## <a name="remarks"></a>Comentários

A propriedade **MSIRMSHUTDOWN** será ignorada se o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
