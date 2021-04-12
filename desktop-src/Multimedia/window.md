---
title: comando de janela
description: O comando Window controla a janela de exibição.
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- Multimídia do Windows de comando da janela
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455101"
---
# <a name="window-command"></a>comando de janela

O comando Window controla a janela de exibição. Você pode usar esse comando para alterar as características de exibição da janela ou fornecer uma janela de destino para o driver a ser usado no lugar da janela de exibição padrão. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

Sinalizador para controlar a janela de exibição. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de janela e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                                                                                                        | Significado                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | tratar o estado do *HWND* hidestate minimizarstate do repositóriostate mostrar maximizado                                                                    | Mostrar minimizedshow [**min**](min.md) noactiveshow Nashow noactivateshow normaltext *Caption*                                             |
| overlay      | fixedhandle defaulthandle *HWND* estado hidestate iconicstate maximizedstate minimizarstate minimizedstate não actionfile noactivatestate normal | Estado RestoreState mostrar maximizedshow minimizedshow [**min**](min.md) noactiveshow Nashow noactivateshow normalstretchtext *Caption* |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszWindowFlags** e seus significados.



| Valor                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixo                            | Desabilita o alongamento da imagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| manipular padrão                   | Especifica que o dispositivo deve definir a janela de exibição de volta para a janela padrão criada durante a operação de [abertura](open.md) . Para dispositivos de sobreposição de vídeo, especifica que o dispositivo deve criar e gerenciar sua própria janela de destino.                                                                                                                                                                                                                                                                                                                                                  |
| *HWND* de identificador                    | Especifica o identificador da janela de destino a ser usada em vez da janela padrão. O parâmetro *HWND* contém o equivalente numérico ASCII do identificador de janela retornado pela função [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Duas instâncias de dispositivo podem usar o mesmo identificador de janela desde que cada instância atualize os pixels de vídeo e imagem na janela como se a outra instância não existisse. Quando a saída de vídeo estiver desabilitada com [setvideo](setvideo.md) "off", um comando de [atualização](update.md) tornará o retângulo de destino uma cor sólida. |
| Mostrar maximizado                   | Maximiza a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostrar [**min**](min.md) noactive | Exibe a janela de destino como um ícone.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Mostrar minimizado                   | Minimiza a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Mostrar na                          | Exibe a janela de destino em seu estado atual; a janela ativa no momento permanece ativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostrar noativação                  | Exibe a janela de destino em seu tamanho e posição mais recentes; a janela ativa no momento permanece ativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Mostrar normal                      | Ativa e exibe a janela de destino em seu tamanho e posição originais. (É o mesmo que o sinalizador "restauração de estado").                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ocultar estado                       | Oculta a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Estado icônico                     | Exibe a janela de destino como um ícone.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Estado maximizado                  | Maximiza a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| minimizar estado                   | Minimiza a janela de destino e ativa a janela de nível superior na lista do Gerenciador de janelas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Estado minimizado                  | Minimiza a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Estado sem ação                  | Exibe a janela de destino em seu estado atual. A janela ativa no momento permanece ativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Estado noactivate                 | Exibe a janela de destino em seu tamanho e estado mais recentes. A janela ativa no momento permanece ativa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| estado normal                     | Ativa e exibe a janela de destino em seu tamanho e posição originais.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| restauração de estado                    | Ativa e exibe a janela de destino em seu tamanho e posição originais.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Mostrar estado                       | Mostra a janela de destino.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Estendi                          | Habilita o alongamento da imagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| *legenda* do texto                   | Especifica a legenda da janela de destino. Se esse texto contiver espaços em branco inseridos, a legenda inteira deverá ser colocada entre aspas. A legenda padrão para a janela padrão está em branco.                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Dispositivos de sobreposição de vídeo normalmente criam e exibem uma janela quando aberto. Se seu aplicativo fornecer uma janela para o driver, seu aplicativo será responsável por gerenciar as mensagens enviadas para a janela.

Como você pode usar o comando [status](status.md) para recuperar o identificador para a janela de exibição do driver, você também pode usar as funções padrão do Gerenciador de janelas (como exibir [janela](/windows/win32/api/winuser/nf-winuser-showwindow)) para manipular a janela.

## <a name="examples"></a>Exemplos

O comando a seguir exibe e define a legenda para a janela de reprodução "filme".

``` syntax
window movie text "Welcome to the Movies" state show
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
</dt> <dt>

[open](open.md)
</dt> <dt>

[reproduzir](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

