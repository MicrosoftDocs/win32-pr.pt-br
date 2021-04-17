---
description: Grava o hive do registro offline especificado em um arquivo.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Função ORSaveHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748903"
---
# <a name="orsavehive-function"></a>Função ORSaveHive

Grava o hive do registro offline especificado em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para o hive do registro offline a ser salvo.

</dd> <dt>

*lpHivePath* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que especifica o nome do arquivo do hive do registro. Este não pode ser o nome de um arquivo existente.

</dd> <dt>

*dwOsMajorVersion* \[ no\]
</dt> <dd>

O número de versão principal do sistema operacional. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Se *dwOsMinorVersion* for 1, o sistema operacional será o Windows XP.<br/> Se o *dwOsMinorVersion* for 2, o sistema operacional será o windows Server 2003 R2, o windows Server 2003 ou o Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Se *dwOsMinorVersion* for 0, o sistema operacional será o windows Server 2008 ou o Windows Vista.<br/> Se *dwOsMinorVersion* for 1, o sistema operacional será o windows Server 2008 R2 ou o Windows 7.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ no\]
</dt> <dd>

O número de versão secundária do sistema operacional. Esse membro pode ser um dos valores a seguir.



| Valor                                                                        | Significado                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Se o *dwOsMajorVersion* for 6, o sistema operacional será o windows Server 2008 ou o Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Se *dwOsMajorVersion* for 5, o sistema operacional será o Windows XP.<br/> Se o *dwOsMajorVersion* for 6, o sistema operacional será o windows Server 2008 R2 ou o Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Se o *dwOsMajorVersion* for 5, o sistema operacional será o windows Server 2003 R2, o windows Server 2003 ou o Windows XP Professional x64 Edition. <br/> Se *dwOsMajorVersion* for 6, o parâmetro *dwOsMinorVersion* deverá ser 0 ou 1. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro. Os códigos de erro possíveis incluem o seguinte:

-   Se o chamador não tiver os direitos de acesso necessários para gravar o arquivo, a função retornará o \_ acesso ao erro \_ negado.
-   Se o arquivo especificado já existir, a função retornará um erro \_ já \_ existe.

## <a name="remarks"></a>Comentários

A função **ORSaveHive** deve ser usada para salvar as alterações feitas em um hive do registro offline. As alterações não são preservadas até que **ORSaveHive** seja chamado para salvar o hive em um arquivo.

Os parâmetros *dwOsMajorVersion* e *dwOsMinorVersion* juntos especificam o formato de destino do arquivo hive do registro. A tabela a seguir resume os números de versão mais recentes do sistema operacional.



| Sistema operacional                    | Número de versão |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5.2            |
| Windows Server 2003                 | 5.2            |
| Windows XP Professional x64 Edition | 5.2            |
| Windows XP                          | 5.1            |



 

Use a função [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) para recuperar informações sobre o sistema operacional atual.

A função **ORSaveHive** bloqueia o hive do registro enquanto está gravando o hive no arquivo e, em seguida, fecha o arquivo e libera o bloqueio. O hive do registro permanece na memória até que seja fechado chamando a função [**ORCloseHive**](orclosehive.md) . É possível fazer outras alterações no hive do registro enquanto ele estiver aberto; no entanto, para preservar essas alterações, o hive deve ser salvo em um novo arquivo, pois a função **ORSaveHive** não substituirá um arquivo existente.

A função **ORSaveHive** pode ser usada para salvar parte do hive do registro offline. A chave especificada no parâmetro *Handle* se torna a chave raiz de um Hive que consiste na chave especificada e todas as suas subchaves.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
