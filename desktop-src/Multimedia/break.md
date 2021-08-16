---
title: Comando break
description: O comando break especifica uma chave para anular um comando que foi invocado usando \ 0034;wait \ 0034; Bandeira. Este comando é um comando do sistema MCI; ele é interpretado diretamente pela MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando break Windows Multimídia
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
# <a name="break-command"></a>Comando break

O comando break especifica uma chave para anular um comando que foi invocado usando o sinalizador "wait". Este comando é um comando do sistema MCI; ele é interpretado diretamente pela MCI.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

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
| no *código de chave virtual* | Especifica a chave que anula um comando que foi iniciado usando o sinalizador "wait". |
| Desligar                   | Desabilita a chave de quebra atual.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Quando a chave de quebra está habilitada e o usuário pressiona a chave identificada pelo código de chave virtual especificado no parâmetro *lpszVirtKey,* o dispositivo retorna o controle para o aplicativo. Se possível, o comando continuará a execução.

## <a name="examples"></a>Exemplos

O comando a seguir define F2 como a chave de quebra para o dispositivo "mysound".

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

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

