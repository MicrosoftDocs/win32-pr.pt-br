---
title: Códigos de erro (UIAutomationCoreApi. h)
description: Este tópico descreve os códigos de erro expostos pela automação da interface do usuário da Microsoft.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008792"
---
# <a name="error-codes-uiautomationcoreapih"></a>Códigos de erro (UIAutomationCoreApi. h)

Este tópico descreve os códigos de erro expostos pela automação da interface do usuário da Microsoft. A lista é classificada alfabeticamente por nome.



| Constante/valor                                                                                                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | Indica que um método foi chamado em um elemento virtualizado ou em um elemento que não existe mais, geralmente porque foi destruído. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | Indica que um método que requer um elemento habilitado, como [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) ou [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), foi chamado em um elemento que foi desabilitado. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | Indica que o método tentou uma operação que não era válida.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt> </dl>                   | Indica que o método [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) foi chamado em um elemento que não tem um ponto clicável.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ E \_ sem suporte**</dt> <dt>0x80040204</dt> </dl>                               | Indica que o provedor não dá suporte explicitamente à propriedade ou ao padrão de controle especificado. A automação da interface do usuário retornará esse código de erro para o chamador sem tentar fornecer um valor padrão ou fazer fallback para outro provedor.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | Indica que ocorreu um problema ao carregar um assembly que contém um provedor do lado do cliente (proxy).<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ E & 0x80131505 de \_ tempo limite**</dt> <dt></dt> </dl>                                                      | Indica que o tempo alocado para um processo ou uma operação expirou.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>UIAutomationCoreApi. h</dt> </dl> |



 

 





