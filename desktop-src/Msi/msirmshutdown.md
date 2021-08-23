---
description: A propriedade MSIRMSHUTDOWN determina como os aplicativos ou serviços que estão usando arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propriedade MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac31a924727217ac86937f4f7ac553717138461e0668a7e79916ffab796f8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012874"
---
# <a name="msirmshutdown-property"></a>Propriedade MSIRMSHUTDOWN

A **propriedade MSIRMSHUTDOWN** determina como os aplicativos ou serviços que estão usando arquivos afetados por uma atualização devem ser desligados para habilitar a instalação da atualização.

## <a name="value"></a>Valor



| Valor                                                                        | Significado                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Processos ou serviços que estão usando arquivos afetados pela atualização são desligados.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Processos ou serviços que estão usando arquivos afetados pela atualização e que não respondem ao Gerenciador de [Reinicialização](../rstmgr/restart-manager-portal.md)são forçados a desligar.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Processos ou serviços que estão usando arquivos afetados pela atualização serão desligados somente se todos eles foram registrados para uma reinicialização. Se qualquer processo ou serviço não tiver sido registrado para uma reinicialização, nenhum processo ou serviço será desligado.<br/> |



 

## <a name="remarks"></a>Comentários

A **propriedade MSIRMSHUTDOWN** será ignorada se o [Gerenciador de Reinicialização](../rstmgr/restart-manager-portal.md) não estiver disponível ou desabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o service pack mínimo exigido por uma versão Windows do instalador.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows 3.1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
