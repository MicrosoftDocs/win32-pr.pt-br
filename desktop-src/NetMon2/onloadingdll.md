---
description: Carrega a DLL do monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Função OnLoadingDLL (Netmon.h)
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
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676866"
---
# <a name="onloadingdll-function"></a>Função OnLoadingDLL

A **função OnLoadingDLL** carrega a DLL do monitor.

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

*hFilterBlob* \[ in, out\]
</dt> <dd>

Um BLOB que o MCSVC usa para corresponder um monitor com NICs disponíveis. Esse parâmetro sempre contém uma solicitação para uma interface [IRTC,](irtc.md) portanto, a maioria dos monitores não precisa adicionar entradas ao BLOB. No entanto, um monitor personalizado pode adicionar critérios de filtro adicionais (por exemplo, que o tipo MAC deve ser Ethernet).

</dd> <dt>

*pCreateFlags* \[ Em\]
</dt> <dd>

Os sinalizadores que indicam como o MCSVC controla a criação de um monitor. Esse parâmetro deve ser um dos seguintes valores:



| Valor                                                                                                                                                                                                            | Significado                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ CRIAM UM POR \_ \_ \_ NETCARD**</dt> </dl>          | O MCSVC garante que apenas uma instância desse monitor exista para cada NIC. Uma segunda instância só poderá ser criada se a primeira for destruída.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ CREATE \_ CONFIGS POR \_ \_ PADRÃO**</dt> </dl> | Se o monitor tiver uma configuração interna padrão, o MCSVC não exigirá que o usuário configure o monitor antes que a instância seja criada.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço do nome padrão do monitor. O MCSVC usa o nome padrão ao criar instâncias do monitor.

Por exemplo, se o nome padrão retornado for "Monitor do Roteador", a primeira instância do monitor será "Monitor do Roteador 1", a segunda será "RouterMonitor2 e assim por diante. Se **NULL** for retornado, o MCSVC usará o nome da DLL.

</dd> <dt>

*ppDescription* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço da descrição do monitor. A descrição é passada para a Ferramenta de Controle do Monitor, que usa a descrição para indicar ao usuário que o monitor existe. Esse parâmetro pode retornar **NULL.**

</dd> <dt>

*ppDefaultScript* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o endereço do script de Formulário HTML padrão usado para configurar o monitor. Embora as instâncias do monitor possam alterar seu próprio script, a maioria dos monitores simplesmente carrega seu script uma vez, de um arquivo. O valor de *ppDefaultScript* pode ser **NULL;** no entanto, o monitor não pode ser configurado externamente ou deve fornecer um script posteriormente. É mais eficiente fornecer um script padrão aqui.

</dd> <dt>

*ppDefaultConfig* \[ out\]
</dt> <dd>

O endereço da cadeia de caracteres padrão usada para configurar o monitor quando ele é criado. Esse parâmetro pode ser definido como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será S \_ OK, que é o mesmo que NOERROR.

Se a função não for bem-sucedida, o MCSVC omiti o monitor especificado de todas as suas listas; depois disso, nenhum monitor desse tipo pode ser criado.

## <a name="remarks"></a>Comentários

A **função OnLoadingDLL** é chamada uma vez pelo MCSVC, quando carrega a DLL pela primeira vez. Em seguida, a DLL fornece os valores padrão que serão usados pelo MCSVC ao criar uma instância de um monitor.

O monitor deve alocar toda a memória necessária para as cadeias de caracteres retornadas ao MCSVC. No retorno, o MCSVC faz cópias de todas as cadeias de caracteres e não tentará liberar as cadeias de caracteres retornadas.

O monitor deve usar funções auxiliares de BLOB para alterar o BLOB de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




