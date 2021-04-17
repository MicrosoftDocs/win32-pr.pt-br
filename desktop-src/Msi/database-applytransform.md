---
description: O método ApplyTransform do objeto de banco de dados aplica a transformação a esse banco de dados.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Método Database. ApplyTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811850"
---
# <a name="databaseapplytransform-method"></a>Método Database. ApplyTransform

O método **ApplyTransform** do objeto de [**banco de dados**](database-object.md) aplica a transformação a esse banco de dados.

## <a name="syntax"></a>Sintaxe


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*storage* 
</dt> <dd>

Caminho para o arquivo de transformação que está sendo aplicado. Este parâmetro é necessário.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Especifica as condições de erro que devem ser suprimidas. Especifique como uma combinação dos valores inteiros a seguir.



| Condição de erro                                                                                                                                                                                                                                                                                                                                                  | Significado                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | Adiciona uma linha que já existe.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | Exclui uma linha que não existe.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | Adiciona uma tabela que já existe.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | Exclui uma tabela que não existe.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | Atualiza uma linha que não existe.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | As páginas de código de transformação e de banco de dados não coincidem e nenhuma página de código neutra.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Cria a tabela temporária de [ \_ transformview](-transformview-table.md).<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **ApplyTransform** atrasa a transformação de tabelas até o último momento possível. As etapas executadas no **ApplyTransform** são transformar imediatamente os catálogos de tabela e de coluna para o banco de dados. Os catálogos de tabela e de coluna são atualizados de acordo com qual tabela é adicionada ou excluída e qual coluna é adicionada (nenhuma exclusão de colunas é permitida). Se uma tabela estiver atualmente carregada na memória e precisar ser transformada, ela será transformada. Caso contrário, o estado da tabela será definido como que exige uma transformação para que, quando a tabela for carregada, ou quando o banco de dados for confirmado, a transformação seja aplicada. A transformação nessa instância significa que os dados reais (linha) da tabela são adicionados, excluídos ou atualizados.

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Backup de banco de dados**](database-object.md)
</dt> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




