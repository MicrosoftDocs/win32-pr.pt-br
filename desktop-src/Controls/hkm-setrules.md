---
title: HKM_SETRULES mensagem (Commctrl.h)
description: Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla quente.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES controles de Windows mensagem
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958705"
---
# <a name="hkm_setrules-message"></a>Mensagem HKM \_ SETRULES

Define as combinações inválidas e a combinação de modificador padrão para um controle de tecla quente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Uma matriz de sinalizadores que especificam combinações de chaves inválidas. Esse parâmetro pode ser uma combinação dos seguintes valores:



| Valor                                                                                                                                                   | Significado                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**AC \_ HKCOMB**</dt> </dl>       | CTRL+ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ NONE**</dt> </dl> | Chaves não modificadas<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | Shift<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ SA**</dt> </dl>       | SHIFT+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | SHIFT+CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | SHIFT+CTRL+ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma matriz de sinalizadores que especificam a combinação de chaves a ser usada quando o usuário ins insula uma combinação inválida. Para obter uma lista de valores de sinalizador modificador, consulte a descrição da [**mensagem \_ HKM GETHOTKEY.**](hkm-gethotkey.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando um usuário insula uma combinação de chaves inválida, conforme definido por sinalizadores especificados em *wParam*, o sistema usa o operador OR bit a bit para combinar as chaves inseridas pelo usuário com os sinalizadores especificados *em lParam*. A combinação de chaves resultante é convertida em uma cadeia de caracteres e, em seguida, exibida no controle de tecla quente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





