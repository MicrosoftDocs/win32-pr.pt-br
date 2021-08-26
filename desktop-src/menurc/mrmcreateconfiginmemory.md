---
title: Função MrmCreateConfigInMemory (MrmResourceIndexer.h)
description: Cria novas informações de configuração do PRI inicializadas (como dados na memória, não como um arquivo) definindo os padrões de qualificador especificados.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menus de função MrmCreateConfigInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b30b4a64313952d48662a82e2f62cdef25106136e7757220668fc094c9258d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011786"
---
# <a name="mrmcreateconfiginmemory-function"></a>Função MrmCreateConfigInMemory

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Cria novas informações de configuração do PRI inicializadas (como dados na memória, não como um arquivo) definindo os padrões de qualificador especificados. A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*. Chame [**MrmFreeMemory com**](mrmfreememory.md) o mesmo ponteiro para liberar essa memória. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*platformVersion* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

A versão da plataforma (*targetOsVersion*) a ser usada para as informações de configuração geradas.

</dd> <dt>

*defaultQualifiers* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista de qualificadores de recurso padrão. Por exemplo, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Tipo: **BYTE \* \***

O endereço de um ponteiro para BYTE. A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*. Chame [**MrmFreeMemory com**](mrmfreememory.md) o ponteiro para BYTE para liberar essa memória.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

O endereço de um ULONG. Em *outputXmlSize*, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do servidor\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

