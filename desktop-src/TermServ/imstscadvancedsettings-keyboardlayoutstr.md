---
title: Propriedade IMsTscAdvancedSettings KeyBoardLayoutStr
description: Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade KeyBoardLayoutStr
- Propriedade KeyBoardLayoutStr Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, propriedade KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644650"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Propriedade IMsTscAdvancedSettings:: KeyBoardLayoutStr

Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.

Se essa propriedade não for definida, o controle usará o layout padrão retornado pela função [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .

Essa propriedade é somente gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do identificador de localidade de entrada ativo.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

A propriedade é um número hexadecimal de oito dígitos na forma de cadeia de caracteres. Os quatro dígitos inferiores representam o identificador de idioma, e os quatro dígitos superiores representam a variação de teclado dentro desse idioma. Portanto, por exemplo, "00000409" representaria o teclado padrão em inglês dos EUA porque "0409" é o identificador de idioma inglês dos EUA. A variação Dvorak do teclado em inglês dos EUA tem um identificador de "00010409". Você pode encontrar os layouts de teclado disponíveis, listados por seus identificadores de layout de teclado, no registro em

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

