---
title: comando de quebra
description: O comando Break especifica uma chave para anular um comando que foi invocado usando o \ 0034; Wait \ 0034; identificar. Esse comando é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando de quebra Windows multimídia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c8609b1364d374d91965816fde2d9c48b750d7bf0b3f6fb2957ed205a85a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375468"
---
# <a name="break-command"></a>comando de quebra

O comando Break especifica uma chave para anular um comando que foi invocado usando o sinalizador "Wait". Esse comando é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Um dos sinalizadores a seguir.



| Valor                 | Significado                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| no *código de chave virtual* | Especifica a chave que anula um comando que foi iniciado usando o sinalizador "Wait". |
| Desligar                   | Desabilita a chave de quebra atual.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Quando a chave de interrupção é habilitada e o usuário pressiona a chave identificada pelo código de chave virtual especificado no parâmetro *lpszVirtKey* , o dispositivo retorna o controle para o aplicativo. Se possível, o comando continua a execução.

## <a name="examples"></a>Exemplos

O comando a seguir define F2 como a chave de interrupção para o dispositivo "mysound".

``` syntax
break mysound on 113
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

