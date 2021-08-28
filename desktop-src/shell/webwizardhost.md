---
description: Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objeto WebWizardHost (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967744"
---
# <a name="webwizardhost-object"></a>Objeto WebWizardHost

Expõe métodos que habilitam páginas HTML que são hospedadas em uma extensão de assistente para se comunicar com o assistente.

## <a name="members"></a>Membros

O objeto **WebWizardHost** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **WebWizardHost** tem esses métodos.



| Método                                                      | Descrição                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancelar**](iwebwizardhost-cancel.md)                     | Simula um clique no botão **Cancelar** .<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou conclui o assistente se não houver outras páginas do lado do cliente.<br/> |
| [**Setheadertext**](iwebwizardhost-setheadertext.md)       | Define o título e o subtítulo que aparecem no cabeçalho do assistente. Em geral, o cliente exibirá o cabeçalho acima do HTML e abaixo da barra de título.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Atualiza os botões **voltar**, **Avançar** e **concluir** no quadro do assistente do cliente.<br/>                                                                                    |



 

### <a name="properties"></a>Propriedades

O objeto **WebWizardHost** tem essas propriedades.



| Propriedade                                               | Tipo de acesso           | Descrição                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Legenda**](iwebwizardhost-caption.md)<br/>   | Leitura/gravação<br/> | Não implementado.<br/>                              |
| [**Propriedade**](iwebwizardhost-property.md)<br/> | Leitura/gravação<br/> | Define ou recupera o valor atual de uma propriedade.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |
| IID<br/>                      | \_WEBWIZARDHOST CLSID<br/>                                                        |



 

 




