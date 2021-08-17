---
title: Modelos de privacidade (Wininet. h)
description: A seguir estão os níveis de privacidade que correspondem às regras para aceitar, aceitar condicionalmente ou não aceitar cookies.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481aa3e9b6b5b5519bac6e458de1acba90f2cfa20dd0a5babac016d0003c70b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955556"
---
# <a name="privacy-templates"></a>Modelos de privacidade

A seguir estão os níveis de privacidade que correspondem às regras para aceitar, aceitar condicionalmente ou não aceitar cookies. Esses níveis correspondem aos níveis de preferência de privacidade definidos na guia privacidade nas opções da Internet. Consulte [privacidade no Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) para obter definições detalhadas.

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**modelo de privacidade \_ \_ sem \_ cookies**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Isso é o mesmo que **bloquear todos os cookies** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**modelo de privacidade \_ \_ alto**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Isso é o mesmo que **alto** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**modelo de privacidade \_ \_ médio \_ alto**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Isso é o mesmo que o **médio \_ alto** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**modelo de privacidade \_ \_ médio**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Isso é o mesmo que **médio** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**modelo de privacidade \_ \_ médio \_ baixo** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Isso é o mesmo que **baixo** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**modelo de privacidade \_ \_ baixo**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Isso é o mesmo que **aceitar todos os cookies** na barra deslizante de preferências de privacidade nas **Opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**modelo de privacidade \_ \_ personalizado**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Definido pelo usuário. Consulte [como criar um arquivo de importação de privacidade personalizado](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) para entender como definir configurações de privacidade personalizadas.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**modelo de privacidade \_ \_ avançado**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Definido pelo usuário. as opções avançadas são definidas na caixa de diálogo de **privacidade avançada Configurações** acessível na guia **privacidade** em **opções da Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**modelo de privacidade \_ \_ máximo**
</dt> <dd> <dl> <dt>

modelo de privacidade \_ \_ baixo
</dt> <dt>



O mesmo **modelo de privacidade é \_ \_ baixo**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

