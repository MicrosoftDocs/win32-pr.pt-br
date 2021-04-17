---
description: O instalador define a propriedade UILevel para o nível da interface do usuário.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Propriedade UILevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768714"
---
# <a name="uilevel-property"></a>Propriedade UILevel

O instalador define a propriedade **UILevel** para o nível da interface do usuário. A interface do usuário interna é habilitada e definida por [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). Essa propriedade é definida como um dos seguintes tipos de dados INSTALLUILEVEL.



| INSTALLUILEVEL          | Valor numérico | Nível da interface do usuário                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ nenhum    | 2             | Instalação Totalmente Silenciosa.             |
| INSTALLUILEVEL \_ básico   | 3             | Progresso simples e tratamento de erros.         |
| INSTALLUILEVEL \_ reduzido | 4             | Interface do usuário criada, caixas de diálogo do assistente suprimidas.     |
| INSTALLUILEVEL \_ completo    | 5             | IU criada com assistentes, progresso, erros. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Interface do usuário](user-interface.md)
</dt> <dt>

[Determinando o nível da interface do usuário de uma ação personalizada](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




