---
description: Retorna o quadro solicitado de uma captura carregada.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Função ExpertGetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826840"
---
# <a name="expertgetframe-function"></a>Função ExpertGetFrame

A função **ExpertGetFrame** retorna o quadro solicitado de uma captura carregada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Um identificador de especialista exclusivo. Monitor de Rede passa o identificador *hExpertKey* para o especialista ao chamar a função [**Run**](run.md) .

</dd> <dt>

*Direção* \[ do no\]
</dt> <dd>

Um valor que identifica como Monitor de Rede procura o quadro.



| Valor                                                                                                                                                                                         | Significado                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**OBTER \_ \_ quadro especificado**</dt> </dl>              | Retornar o quadro solicitado.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**OBTER \_ \_ próximo quadro avançar \_**</dt> </dl>    | Retornar o próximo quadro.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**OBTER \_ quadro \_ próximo \_ atrás**</dt> </dl> | Retornar o quadro anterior.<br/>  |



 

</dd> <dt>

*RequestFlags* \[ no\]
</dt> <dd>

Os sinalizadores que especificam como Monitor de Rede devem tratar a solicitação. Especifique um ou mais dos sinalizadores a seguir.



| Valor                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**SINALIZADORES \_ adiados \_ para o \_ filtro de interface do usuário \_**</dt> </dl> | Antes de aplicar o parâmetro de filtro de exibição do especialista que é especificado em *hFilter*, aplique o filtro de exibição que monitor de rede está usando quando o especialista é iniciado.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**\_Propriedades de anexação de sinalizadores \_**</dt> </dl>      | As propriedades que todos os analisadores de protocolo encontram com as seções reivindicadas desse quadro são anexadas ao quadro. Se o sinalizador não for definido, o campo **lpPropertyTable** da estrutura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (retornado por **PEFrameDescriptor**) será definido como **NULL**.<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[ no\]
</dt> <dd>

O número do quadro solicitado.

</dd> <dt>

*hFilter* \[ no\]
</dt> <dd>

Um identificador para o filtro de exibição de especialista. Se o especialista não tiver um filtro de exibição, defina o parâmetro como **NULL**.

</dd> <dt>

*pEFrameDescriptor* \[ fora\]
</dt> <dd>

A estrutura [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) que, no retorno, descreve o quadro. O especialista deve alocar e liberar a memória que essa estrutura usa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha. Se o valor de retorno for NMERR \_ especialista \_ , o especialista deverá limpar e retornar imediatamente; o usuário anulou a execução do especialista.

## <a name="remarks"></a>Comentários

Se você definir sinalizadores \_ anexar \_ Propriedades, a chamada exigirá mais recursos do que se você não definir o sinalizador. Se o sinalizador não estiver definido, um ponteiro apontará para o quadro bruto e para os dados sobre o quadro. Se esse sinalizador for definido, Monitor de Rede anexará todas as propriedades ao quadro chamando todos os analisadores que alegam uma parte do quadro. Isso pode ser um processo lento.

Os especialistas não devem definir o \_ sinalizador de propriedades anexar sinalizadores \_ , a menos que os especialistas exijam as propriedades que os analisadores anexam ao quadro. Se possível, os especialistas devem chamar a função **ExpertGetFrame** sem o sinalizador e, em seguida, extrair os dados necessários diretamente do quadro.

Se o especialista chamar **ExpertGetFrame** sem o \_ sinalizador de propriedades de anexação de sinalizadores \_ e exigir as propriedades associadas a esse quadro (um evento, por exemplo), o especialista chamará **ExpertGetFrame** com os mesmos parâmetros, exceto para o seguinte:

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

O uso do código anterior garante que o especialista obtenha o quadro necessário sem precisar chamar o código de filtro novamente.

Você pode definir o parâmetro *hFilter* como um **LPVOID**. Se existir, o quadro retornado passará por esse filtro. Se o especialista não tiver um filtro de exibição para passar para a função (se *hFilter* for **nulo** ), o quadro retornado não será filtrado.

A função **ExpertGetFrame** só pode ser chamada por especialistas que implementam a função [**executar**](run.md) ou [**Configurar**](configure.md) exportação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




