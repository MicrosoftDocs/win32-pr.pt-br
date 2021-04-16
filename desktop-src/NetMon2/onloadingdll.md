---
description: Carrega a DLL do monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Função OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787045"
---
# <a name="onloadingdll-function"></a>Função OnLoadingDLL

A função **OnLoadingDLL** carrega a DLL do monitor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFilterBlob* \[ entrada, saída\]
</dt> <dd>

Um BLOB que o MCSVC usa para corresponder a um monitor com NICs disponíveis. Esse parâmetro sempre contém uma solicitação para uma interface [IRTC](irtc.md) , de modo que a maioria dos monitores não precisa adicionar nenhuma entrada ao blob. No entanto, um monitor personalizado pode adicionar critérios de filtro adicionais (por exemplo, que o tipo de MAC deve ser Ethernet).

</dd> <dt>

*pCreateFlags* \[ no\]
</dt> <dd>

Os sinalizadores que indicam como o MCSVC controla a criação de um monitor. Esse parâmetro deve ser um dos seguintes valores:



| Valor                                                                                                                                                                                                            | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ criar \_ um \_ por \_ Netcard**</dt> </dl>          | O MCSVC garante que apenas uma instância desse monitor exista para cada NIC. Uma segunda instância só poderá ser criada se a primeira for destruída.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**\_ \_ configurações de MCS Create \_ por \_ padrão**</dt> </dl> | Se o monitor tiver uma configuração interna padrão, o MCSVC não exigirá que o usuário configure o monitor antes que a instância seja criada.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço do nome padrão do monitor. O MCSVC usa o nome padrão ao criar instâncias do monitor.

Por exemplo, se o nome padrão retornado for "monitor do roteador", a primeira instância do monitor será "monitor do roteador 1", o segundo seria "RouterMonitor2 e assim por diante. Se **NULL** for retornado, o MCSVC usará o nome da dll.

</dd> <dt>

*ppDescription* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço da descrição do monitor. A descrição é passada para a ferramenta de controle de monitor, que usa a descrição para indicar ao usuário que o monitor existe. Esse parâmetro pode retornar **NULL**.

</dd> <dt>

*ppDefaultScript* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço do script de formulário HTML padrão usado para configurar o monitor. Embora as instâncias do monitor possam alterar seu próprio script, a maioria dos monitores simplesmente carrega seu script uma vez, de um arquivo. O valor de *ppDefaultScript* pode ser **nulo**; no entanto, o monitor não pode ser configurado externamente ou deve fornecer um script mais tarde. É mais eficiente fornecer um script padrão aqui.

</dd> <dt>

*ppDefaultConfig* \[ fora\]
</dt> <dd>

O endereço da cadeia de caracteres padrão usada para configurar o monitor quando ele é criado. Esse parâmetro pode ser definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será S Ok, o \_ que é o mesmo que NOERROR.

Se a função não for bem-sucedida, o MCSVC omitirá o monitor especificado de todas as suas listas; Depois, nenhum monitor desse tipo pode ser criado.

## <a name="remarks"></a>Comentários

A função **OnLoadingDLL** é chamada uma vez por MCSVC, quando carrega pela primeira vez a dll. Em seguida, a DLL fornece os valores padrão que serão usados pelo MCSVC ao criar uma instância de um monitor.

O monitor deve alocar toda a memória necessária para as cadeias de caracteres retornadas para o MCSVC. No retorno, o MCSVC faz cópias de todas as cadeias de caracteres e não tentará liberar as cadeias de caracteres retornadas.

O monitor deve usar funções auxiliares de BLOB para alterar o BLOB de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




