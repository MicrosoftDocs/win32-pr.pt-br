---
description: O método FileHash do objeto instalador usa o caminho para um arquivo e retorna um hash de 128 bits desse arquivo. As informações de hash do arquivo são retornadas como um objeto de registro. O hash do arquivo de 128 bits inteiro é retornado como campos de propriedade IntegerData de 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Método Installer. FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750612"
---
# <a name="installerfilehash-method"></a>Método Installer. FileHash

O método **FileHash** do [**objeto instalador**](installer-object.md) usa o caminho para um arquivo e retorna um hash de 128 bits desse arquivo. As informações de hash do arquivo são retornadas como um [**objeto de registro**](record-object.md). O hash do arquivo de 128 bits inteiro é retornado como campos de propriedade [**IntegerData**](record-integerdata.md) de 4 32 bits.

Os valores retornados no [**objeto de registro**](record-object.md) correspondem aos quatro campos da estrutura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) retornados por [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). A numeração de quatro campos é baseada em 1 na [tabela MsiFileHash](msifilehash-table.md).

-   O campo 1 corresponde à coluna HashPart1.
-   O campo 2 corresponde à coluna HashPart2.
-   O campo 3 corresponde à coluna HashPart3.
-   O campo 4 corresponde à coluna HashPart4.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilePath* 
</dt> <dd>

Caminho para o arquivo cujo hash deve ser feito.

</dd> <dt>

*Opções* 
</dt> <dd>

Reservado para uso futuro.

O valor desse parâmetro deve ser 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará um [**objeto de registro**](record-object.md) que contém o hash do arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de versão de arquivo padrão](default-file-versioning.md)
</dt> <dt>

[Gerenciar tamanhos e versões de arquivo](manage-file-sizes-and-versions.md)
</dt> <dt>

[Tabela MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




