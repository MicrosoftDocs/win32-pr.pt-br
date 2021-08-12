---
title: Propriedade IMsTscAdvancedSettings KeyBoardLayoutStr
description: Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout do teclado) a ser usado para a conexão.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Propriedade KeyBoardLayoutStr Serviços de Área de Trabalho Remota
- A propriedade KeyBoardLayoutStr Serviços de Área de Trabalho Remota , interface IMsTscAdvancedSettings
- Interface IMsTscAdvancedSettings Serviços de Área de Trabalho Remota , propriedade KeyBoardLayoutStr
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
ms.openlocfilehash: 3c87cb55b22658f704b328a51435ca2554d4c6574e25484253f9899475918642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606173"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Propriedade IMsTscAdvancedSettings::KeyBoardLayoutStr

Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout do teclado) a ser usado para a conexão.

Se essa propriedade não estiver definida, o controle usará o layout padrão retornado pela [**função GetKeyboardLayout.**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout)

Essa propriedade é somente gravação.

## <a name="syntax"></a>Sintaxe


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

A propriedade é um número hexadecimal de oito dígitos no formato de cadeia de caracteres. Os quatro dígitos inferiores representam o identificador de idioma e os quatro dígitos superiores representam a variação de teclado dentro desse idioma. Portanto, por exemplo, "00000409" representaria o teclado padrão em inglês dos EUA porque "0409" é o identificador de idioma inglês dos EUA. A variação do Dvorak do teclado inglês dos EUA tem um identificador de "00010409". Você pode encontrar os layouts de teclado disponíveis, listados por seus identificadores de layout de teclado, no Registro em

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

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

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

